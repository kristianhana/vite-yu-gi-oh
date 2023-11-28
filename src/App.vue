<script>
import axios from "axios";
import { store } from "./store.js";

import AppHeader from "./components/AppHeader.vue";
import AppCardsList from "./components/AppCardsList.vue";

export default {
  data() {
    return {
      store
    } 
  },
  created() {
    axios.get(this.store.apiUrl).then((resp) => {
      this.store.cards = resp.data.data;
      console.log(resp);
    });
  },
  components: { AppHeader, AppCardsList },
}
</script>

<template>
  <AppHeader/>
  <AppCardsList/>
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
