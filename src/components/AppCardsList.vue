<script>
import { store } from "../store.js";
import AppLoader from "../components/AppLoader.vue";
import AppCard from "../components/AppCard.vue";



export default {
    data() {
        return {
            store,
        };
    },
    components: { AppLoader, AppCard },
};
</script>

<template>
    <div class="container">

        <AppLoader v-if="store.loading"/>

        <h5 class="badge text-bg-dark p-3 d-flex">FOUND number CARDS</h5>

        <div class="row row-cols-5 g-4 p-3">
            <div class="col" v-for="cardsInfo in store.cards">
                <AppCard :cardsInfo="cardsInfo" />
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

.container {
    padding: 1rem;
    background-color: white;
}
</style>
