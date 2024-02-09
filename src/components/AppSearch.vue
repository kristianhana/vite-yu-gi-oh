<script>
import { store } from "../store.js";
export default {
    data() {
        return {
            store,
            archetypes: [
                "Alien",
                "Ally of Justice",
                "Ancient Gear",
                "Blue-Eyes",
                "Dark Magician",
            ]
        };
    },
};
</script>

<template>
    <div class="input-group mb-3 mt-3 container-sm w-25">
        <select class="form-select" id="inputGroupSelect02" v-model="store.searchText" @change="$emit('searchArchetype')">
            <option value="" selected>All</option>
            <option v-for="archetype in archetypes" :value="archetype">
                {{ archetype }}
            </option>
        </select>

        <label class="input-group-text" for="inputGroupSelect02">Options</label>

    </div>
</template>

<style lang="scss" scoped></style>
