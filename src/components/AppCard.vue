<script>
export default {
    props: {
        cardsInfo: Object,
    },
};
</script>

<template>
    <main>
        <div class="card h-100">
            <img class="card-img-top" :src="cardsInfo.card_images[0].image_url_small" alt="">
            <div class="card-body text-center">
                <h5 class="card-title">{{ cardsInfo.name }}</h5>
                <p class="card-text">{{ cardsInfo.archetype ? cardsInfo.archetype : "Nessun archetipo" }}</p>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped></style>

