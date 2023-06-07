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
        <div>{{ details.archetype }}</div>
    </div>
</template>

<style scoped lang="scss">
.SingleCard {
    width: 300px;
    height: 300px;
    border: 5px solid white;
    text-align: center;
}

h4 {
    color: white;
}
</style>