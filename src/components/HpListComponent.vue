<template lang="html">
  <div>
    <ul>
      <list-item v-for="(hpData, index) in hpData" :hpData="hpData" :key="index"></list-item>
    </ul>
  </div>
</template>

<script>
import ListItem from './ListItem.vue';

export default {
  name: 'hp-data',
  props: ['hpData'],
  components: {
    "list-item": ListItem
  }
}
</script>

<style lang="css" scoped>
</style>
