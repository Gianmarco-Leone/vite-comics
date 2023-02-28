<script>
export default {
  props: {
    cardItem: Object,
  },
};
</script>

<template>
  <div class="card">
    <img :src="cardItem.thumb" />
    <div class="card-text">
      <span> {{ cardItem.series }} </span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  padding: 1rem;
  width: calc(100% / 6);

  img {
    width: 162px;
    height: 162px;
    object-position: top;
    cursor: pointer;
  }

  .card-text {
    margin-top: 1rem;
    min-height: 2.5rem;

    span {
      color: #fff;
      font-size: 0.7rem;
    }
  }
}
</style>
