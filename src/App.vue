<script>
import { store } from './store.js';
import axios from 'axios';
import AppHeader from './components/AppHeader.vue'
import CharactersList from './components/CharactersList.vue'
export default {
  components: {
    AppHeader,
    CharactersList
  },
  data() {
    return {
      store
    }
  },
  methods: {
    getCharacters() {
      axios.get(store.apiURL)
        .then(res => {
          store.characterList = res.data.data;
        })
        .catch(err => {
          console.log(err);
        })
    }
  },
  created() {
    this.getCharacters()
  }
}
</script>

<template>
  <AppHeader message="Yu-Gi-Oh Api" />
  <CharactersList />
</template>

<style lang ="scss">
@use './styles/general.scss' as *;
</style>
