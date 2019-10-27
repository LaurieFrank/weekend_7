<template lang="html">
  <div>
    <ul>
      <list-item v-for="(character, index) in hpCharacters" :character="character" :key="index"></list-item>
    </ul>
  </div>
</template>

<script>
import ListItem from './ListItem.vue';

export default {
  name: 'hp-list-component',
  props: ['hpCharacters'],
  components: {
    "list-item": ListItem
  }
}
</script>

<style lang="css" scoped>
</style>
