<template lang="html">
  <div v-if="hpData">
    <h3>{{hpdata.name}}</h3>
    <p>Patronus: {{hpdata.patronus}}</p>
  </div>
</template>

<script>
export default {
  name: "character-detail",
  props: ["hpData"]
}
</script>

<style lang="css" scoped>
</style>
