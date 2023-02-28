<script>
// Importo i vari componenti
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";

// Importo il file index che raccoglie tutti i miei file data,
// alla fine del percorso potrei anche omettere /index.js
// perchè i file index sono i primi che vengono letti
import { headerLinks, comics } from "./data/index.js";

export default {
  data() {
    return {
      // headerLinks: headerLinks, => che è uguale a scrivere
      headerLinks,
      // comics: comics, => che è uguale a scrivere
      comics,
    };
  },

  // Richiamo i vari componenti
  components: {
    AppHeader,
    AppContent,
    AppFooter,
  },
};
</script>

<template>
  <AppHeader :listLinks="headerLinks" />
  <main>
    <AppContent :cardList="comics" />
  </main>
  <AppFooter />
</template>

<style lang="scss">
@use "./assets/scss/general.scss";
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap");

body {
  font-family: "Roboto", sans-serif;
}
</style>
