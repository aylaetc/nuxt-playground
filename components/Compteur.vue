<template>
  <div>

    <button type="button" @click="compteur++">
      {{compteur}} personnes sont d'accord
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      compteur: 454
    }
  }
}
</script>
<style>
  button{
    font-size: 2em;
    margin:20px;
  }
</style>
