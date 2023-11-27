<script>
import { store } from "../store.js";
import AppCard from "../components/AppCard.vue";
import AppLoader from "../components/AppLoader.vue";

export default {
    data() {
        return {
            store,
        };
    },
    activeIndex: 0,
    components: { AppCard, AppLoader },
};
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col" v-for="(cardsInfo, index) in store.name">
                <AppCard :cardsInfo="cardsInfo" />
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>
