<template>
  <div class="container">
    <div>
      <h1 class="title">
        Mes projets
      </h1>

      <ul>
        <li v-for="projet in projets" :key="projet.slug" ><nuxt-link :to="`/projets/${projet.slug}`">{{projet.title}}</nuxt-link></li>
      </ul>


    </div>
  </div>
</template>

<script>
export default {

  async asyncData({$content}) {
    const projets = await $content('projets').fetch()

    return {
      projets
    }
  }
}
</script>
