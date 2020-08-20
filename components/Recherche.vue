<template>
 <aside class="search">
   <input type="text" v-model="search" @keyup="executeSearch()">
   <div class="results" v-if="projets.length>0">
     <article v-for="result in projets">
       <nuxt-link :to="`/projets/${result.slug}`" @click="search=''">{{result.title}}</nuxt-link>
     </article>
   </div>
 </aside>
</template>

<script>
export default {
  data() {
    return {
      search: "",
      projets:[]
    }
  },
  methods: {
    async executeSearch() {
      this.loading=true
      this.projets = await this.$content('projets').search(this.search).fetch()
      this.loading=false
    }
  }
}
</script>
<style lang="scss">
  .search{
    float:right;
  }
  .results{
    position:absolute;
    background-color: blue;
    right:10px;
    padding:20px;
    max-width: 200px;
  }
</style>
