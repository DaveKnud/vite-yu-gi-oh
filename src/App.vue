<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue'

export default {
  components: {
    AppHeader
  }
}
</script>

<template>
  <AppHeader message="CiaoCiao" />
</template>

<style lang ="scss">
@use './styles/general.scss' as *;
</style>
