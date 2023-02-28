<script>
import AppCard from "./AppCard.vue";

export default {
  props: {
    cardList: Array,
  },
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
          <AppCard v-for="card in cardList" :cardItem="card" />
        </div>
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

  .jumbotron {
    height: 40vh;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    background-position: top;
    background-repeat: no-repeat;
  }

  .container {
    position: relative;

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
