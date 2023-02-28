<script>
export default {
  props: {
    cardItem: Object,
  },
};
</script>

<template>
  <div class="card">
    <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
    <div class="card-text">
      <span> {{ cardItem.series }} </span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  //  debug
  padding: 1rem;
  width: calc(100% / 6);

  .card-text {
    margin-top: 1rem;
    min-height: 2rem;

    span {
      color: #fff;
      font-size: 0.7rem;
    }
  }
}
</style>
