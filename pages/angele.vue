<template>
  <div class="container">
    <div>
      <h1 class="title">
        Angèle
      </h1>
      <h2>C'est la plus belle de toutes</h2>
      <nuxt-link to="/">Retour</nuxt-link>
      <hr>
      <Compteur></Compteur>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
