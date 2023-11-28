<script>
import axios from "axios";
import { store } from "./store.js";

import AppHeader from "./components/AppHeader.vue";
import AppCardsList from "./components/AppCardsList.vue";
import AppSearch from "./components/AppSearch.vue";


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

  components: { AppHeader, AppCardsList, AppSearch},

  methods: {
     handleSearch() {
      console.log("cerca");
      axios.get(this.store.apiUrl, {
        params: {
          archetype: this.store.searchText,
        }
      })
      .then((resp) => {
        this.store.cards = resp.data.data;
        console.log(resp); 
      })
     }
  }
}
</script>

<template>
  <AppHeader/>
  <AppSearch @searchArchetype="handleSearch"/>
  <AppCardsList/>
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
