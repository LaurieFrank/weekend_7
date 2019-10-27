<template lang="html">
  <div v-if="character">
    <h3>{{character.name}}</h3>
    <p>Patronus: {{character.patronus}}</p>
  </div>
</template>

<script>
export default {
  name: "character-detail",
  props: ["character"]
}
</script>

<style lang="css" scoped>
</style>
