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
    components: { AppLoader, AppCard},
};
</script>

<template>
    <div class="container text-center">
        <div class="row row-cols-5 g-4 p-3 mt-5">
            <div class="col" v-for="cardsInfo in store.cards">
                <AppCard :cardsInfo="cardsInfo"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    background-color: white;
}
</style>
