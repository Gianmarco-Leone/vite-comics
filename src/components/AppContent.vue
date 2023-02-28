<script>
// Importo il componente della singola card
import AppCard from "./AppCard.vue";

export default {
  // Recupero lista dati comics
  props: {
    cardList: Array,
  },

  // Richiamo componente singola card
  components: {
    AppCard,
  },
};
</script>

<template>
  <section>
    <div class="jumbotron"></div>
    <div class="container">
      <span class="jumbotron-label">CURRENT SERIES</span>
      <div class="content">
        <div class="card-container">
          <!-- Componente Card -->
          <AppCard v-for="card in cardList" :cardItem="card" />
        </div>

        <!-- Bottone LOAD MORE -->
        <div class="text-center">
          <button type="button" class="primary-btn">LOAD MORE</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../assets/scss/general.scss" as *;
@use "../assets/scss/mixin.scss" as *;

section {
  background-color: #222;

  // Sfondo Jumbotron
  .jumbotron {
    height: 40vh;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    background-position: top;
    background-repeat: no-repeat;
  }

  .container {
    position: relative;

    // Etichetta blu tra jumbotron e sezione cards
    .jumbotron-label {
      background-color: #0282f9;
      padding: 0.5rem 1rem;
      font-size: 1.2rem;
      font-weight: bold;
      color: #fff;
      cursor: pointer;
      position: absolute;
      top: -1rem;
    }
  }

  /************  
  SEZIONE CARDS
  *************/
  .content {
    padding: 3rem 0;

    .card-container {
      @include flex-center();
      flex-wrap: wrap;
    }

    .primary-btn {
      background-color: #0282f9;
      padding: 0.5rem;
      font-weight: bold;
      color: #fff;
      cursor: pointer;
    }
  }
}
</style>
