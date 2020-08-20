<template>
 <nav class="main-nav">
   <nuxt-link to="/">Accueil</nuxt-link>
   <nuxt-link to="/projets">Projets</nuxt-link>
   <Recherche></Recherche>
 </nav>
</template>

<script>
export default {

}
</script>
<style lang="scss">
  .main-nav{
    color:white;
    margin-bottom: 20px;
    a{
      color: white;
    }
    background-color: black;
    padding:30px;
    font-weight: bold;
    text-align: center;
  }
</style>
