<script>
import { store } from "../store.js";
export default {
    data() {
        return {
            store,
        };
    },
};
</script>

<template>
    <div class="input-group mb-3 mt-3 container-sm">
        <select class="form-select" id="inputGroupSelect02" v-model="store.searchText" @change="$emit('searchArchetype')">
            <option value="Alien">Alien</option>
            <option value="Ally of Justice">Ally of Justice</option>
            <option value="Ancient Gear">Ancient Gear</option>
        </select>

        <label class="input-group-text" for="inputGroupSelect02">Options</label>

    </div>
</template>

<style lang="scss" scoped></style>
