<script>
export default {
    name: 'SingleCharacter',
    props: {
        details: Object
    }
}
</script>

<template>
    <div class="SingleCard">
        <img :src="details.card_images[0].image_url_small" alt="info.image">
        <h4>{{ details.name }}</h4>
        <div>stato personaggio</div>
        <div>specie personaggio</div>
    </div>
</template>

<style scoped lang="scss">
h1 {
    font-weight: 700;
}
</style>