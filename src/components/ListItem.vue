<template lang="html">
  <li @click="handleClick">{{hpData.name}}</li>
</template>

<script>
import {eventBus} from "../main.js";

export default {
  name: 'list-item',
  props: ['hpData'],
  methods: {
    handleClick(){
      eventBus.$emit("character-selected", this.hpData);
    }
  }
}
</script>

<style lang="css" scoped>
</style>
