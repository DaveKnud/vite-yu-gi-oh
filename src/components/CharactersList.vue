<script>
import { store } from './../store.js';

import SingleCharacter from './SingleCharacter.vue';
export default {
    name: 'CharactersList',
    components: {
        SingleCharacter
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <section class="container">
        <SingleCharacter v-for="character in store.characterList" :details="character" />
    </section>
</template>

<style scoped lang="scss">
h4 {
    font-weight: 700;
}
</style>


