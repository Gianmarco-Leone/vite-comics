<script>
export default {};
</script>

<template>
  <!-- Parte superiore Footer -->
  <div class="footer-top">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="card">
            <img
              src="../assets/img/buy-comics-digital-comics.png"
              alt="Digital comics"
            />
            <span>DIGITAL COMICS</span>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <img
              src="../assets/img/buy-comics-merchandise.png"
              alt="Digital comics"
            />
            <span>DC MERCHANDISE</span>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <img
              src="../assets/img/buy-comics-subscriptions.png"
              alt="Digital comics"
            />
            <span>SUBSCRIPTION</span>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <img
              src="../assets/img/buy-comics-shop-locator.png"
              alt="Digital comics"
            />
            <span>COMIC SHOP LOCATOR</span>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <img
              src="../assets/img/buy-dc-power-visa.svg"
              alt="Digital comics"
            />
            <span>DC POWER VISA</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mixin.scss" as *;

.footer-top {
  height: 100px;
  background-color: #0282f9;
  position: relative;
  z-index: 1;

  .container {
    height: 100%;

    .row {
      height: 100%;
      @include flex-center();
      padding: 0 2rem;

      .col {
        height: 100%;
        width: calc(100% / 5);

        .card {
          @include flex-center();
          height: 100%;
          font-size: 0.8rem;

          img {
            width: 2rem;
          }

          span {
            display: block;
            color: #fff;
            margin-left: 1rem;
          }
        }
      }
    }
  }
}
</style>
