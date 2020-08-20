<template>
    <div>
      <nuxt-content :document="projet"></nuxt-content>
    </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const projet = await $content(`projets/${params.slug}`).fetch()

    return {
      projet
    }
  }
}
</script>
