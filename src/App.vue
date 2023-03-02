<script>

// IMPORT DEL COMPONENTE
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import axios from "axios";
import { store } from "./assets/store";

// DEFINIZIONE DEL COMPONENTE IN PAGINA
export default {

  components: {
    AppHeader, AppMain,
  },

  return: {
    store,
  },

  created() {
    axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0")
      .then((response) => { store.cards = response; })
  }
};
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
</template>


<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>