<script>
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter,
  },
};
</script>

<template>
  <AppHeader />
  <main>
    <AppContent />
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
