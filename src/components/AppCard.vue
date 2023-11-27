<script>
export default {
    props: {
        cardsInfo: Array,
    },
    index: 0,
};
</script>

<template>
    <main>
        <div>
            <img :src="cardsInfo.data.data[index].card_images[index].image_url" alt="">
            <p>{{ cardsInfo.data.data[index].archetype }}</p>
        </div>
    </main>
</template>

<style lang="scss" scoped>

</style>

