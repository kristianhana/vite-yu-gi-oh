<script>
import axios from "axios";
import { store } from "./store.js";

import AppHeader from "./components/AppHeader.vue";
import AppCardList from "./components/AppCardsList.vue";

export default {
  data() {
    return {
      store
    }
  },
  components: { AppHeader, AppCardList},
}
</script>

<template>
  <AppHeader/>
  <AppCardsList/>
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
