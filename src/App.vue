<script>
// Importo i vari componenti
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";

// Importo il file index che raccoglie tutti i miei file data,
// alla fine del percorso potrei anche omettere /index.js
// perchè i file index sono i primi che vengono letti
import { headerLinks, comics, footerMenus } from "./data/index.js";

export default {
  data() {
    return {
      // headerLinks: headerLinks, => che è uguale a scrivere
      headerLinks,
      // comics: comics, => che è uguale a scrivere
      comics,
      // footerMenus: footerMenus, => che è uguale a scrivere
      footerMenus,
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
  <AppFooter :menus="footerMenus" />
</template>

<style lang="scss">
@use "./assets/scss/general.scss";
</style>
