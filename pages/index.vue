<template>
    <div>
      <nuxt-content class="page" :document="page"></nuxt-content>

      <section class="experiences">
          <Experience :experience="experience" v-for="experience in experiences" :key="experience.title"></Experience>
      </section>
      <nuxt-link to="/projets">Voir tous mes projets cools</nuxt-link>
    </div>
</template>

<script>
export default {

  async asyncData({$content}) {
    const experiences = await $content('experiences').sortBy('start', 'desc').fetch()
    const page = await $content('home').fetch()

    return {
      experiences, page
    }
  }
}
</script>

<style lang="scss">

  .page{
    text-align: center;
    margin-bottom: 40px;
    img{
      width:30%;
    }
}

</style>
