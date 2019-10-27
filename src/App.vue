<template>
  <div>
    <h1>Harry Potter Characters</h1>
    <hp-list-component :hpCharacters="hpCharacters"></hp-list-component>
    <character-detail :character="selectedCharacter"></character-detail>
  </div>
</template>

<script>
import HpListComponent from "./components/HpListComponent.vue";
import CharacterDetail from "./components/CharacterDetail.vue";
import {eventBus} from "./main.js";

export default {
  name: 'app',
      data() {
        return {
          hpCharacters: [],
          selectedCharacter: null
        };
      },

mounted(){
  eventBus.$on("character-selected", (character) => {
    this.selectedCharacter = character;
  })

  fetch('http://hp-api.herokuapp.com/api/characters')
  .then(response => response.json())
  .then(hpCharacters => this.harryPotterCharacters = hpCharacters)
  // .then(hpCharacters => console.log(hpCharacters))
},
  components: {
    "hp-list-component": HpListComponent,
    "character-detail": CharacterDetail
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
