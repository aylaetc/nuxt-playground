<template>
  <article class="experience">
    <h1>{{experience.title}}</h1>
    <p>De {{experience.start}} à {{experience.end}} <span class="place">{{experience.place}}</span></p>
    <p>{{experience.description}}</p>
  </article>
</template>

<script>
export default {
  props: {
    experience: {
      type: Object,
      required: true,
    }
  }
}
</script>
<style lang="scss">
  .experience{
    margin:10px;
    h1{
      font-size: 2.1em;
    }
    .place{
      color: gray;
    }
  }
</style>
