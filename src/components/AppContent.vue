<script>
export default {};
</script>

<template>
  <section>
    <div class="container">
      <div class="content">
        <span> --> Content goes here &lt;-- </span>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mixin.scss" as *;

section {
  @include flex-center("vertical");
  min-height: 150px;
  background-color: #222;

  .content {
    // debug
    width: 1200px;
    span {
      color: #fff;
      font-size: 1.5rem;
      font-weight: bold;
    }
  }
}
</style>
