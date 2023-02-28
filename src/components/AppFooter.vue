<script>
// Importo componente fascia azzurra
import AppFooterTop from "./AppFooterTop.vue";

export default {
  // Richiamo componente fascia azzurra
  components: {
    AppFooterTop,
  },
};
</script>

<template>
  <footer>
    <!-- Componente fascia azzurra -->
    <AppFooterTop />

    <!-- PARTE CENTRALE -->
    <div class="footer-main">
      <div class="container">
        <!-- Prima colonna -->
        <div class="my-footer-col">
          <span class="footer-list-title"> DC COMICS </span>

          <ul>
            <li>
              <a href="#">Characters</a>
            </li>
            <li>
              <a href="#">Commics</a>
            </li>
            <li>
              <a href="#">Movies</a>
            </li>
            <li>
              <a href="#">TV</a>
            </li>
            <li>
              <a href="#">Games</a>
            </li>
            <li>
              <a href="#">Videos</a>
            </li>
            <li>
              <a href="#">News</a>
            </li>
          </ul>

          <span class="footer-list-title"> SHOP </span>

          <ul>
            <li>
              <a href="#">Shop DC</a>
            </li>
            <li>
              <a href="#">Shop DC Collectibles</a>
            </li>
          </ul>
        </div>

        <!-- Seconda colonna -->
        <div class="my-footer-col">
          <span class="footer-list-title"> DC </span>

          <ul>
            <li>
              <a href="#">Terms Of Use</a>
            </li>
            <li>
              <a href="#">Privacy policy (New)</a>
            </li>
            <li>
              <a href="#">Ad Choices</a>
            </li>
            <li>
              <a href="#">Advertising</a>
            </li>
            <li>
              <a href="#">Jobs</a>
            </li>
            <li>
              <a href="#">Subscriptions</a>
            </li>
            <li>
              <a href="#">Talent Workshops</a>
            </li>
            <li>
              <a href="#">CPSC Cerificates</a>
            </li>
            <li>
              <a href="#">Ratings</a>
            </li>
            <li>
              <a href="#">Shop Help</a>
            </li>
            <li>
              <a href="#">Contact Us</a>
            </li>
          </ul>
        </div>

        <!-- Terza colonna -->
        <div class="my-footer-col">
          <span class="footer-list-title"> SITES </span>

          <ul>
            <li>
              <a href="#">DC</a>
            </li>
            <li>
              <a href="#">MAD Magazine</a>
            </li>
            <li>
              <a href="#">DC Kids</a>
            </li>
            <li>
              <a href="#">DC Universe</a>
            </li>
            <li>
              <a href="#">DC Power Visa</a>
            </li>
          </ul>
        </div>

        <!-- Logo DC di sfondo -->
        <img src="../assets/img/dc-logo-bg.png" alt="Logo background" />
      </div>
    </div>

    <!-- PARTE INFERIORE -->
    <div class="footer-bottom">
      <div class="container">
        <button type="button" class="outlined-btn">SIGN-UP NOW!</button>

        <ul>
          <li>
            <span>FOLLOW US</span>
          </li>
          <li>
            <a href="#">
              <img
                src="../assets/img/footer-facebook.png"
                alt="Facebook icon"
              />
            </a>
          </li>
          <li>
            <a href="#">
              <img src="../assets/img/footer-twitter.png" alt="Twitter icon" />
            </a>
          </li>
          <li>
            <a href="#">
              <img src="../assets/img/footer-youtube.png" alt="YouTube icon" />
            </a>
          </li>
          <li>
            <a href="#">
              <img
                src="../assets/img/footer-pinterest.png"
                alt="Pinterest icon"
              />
            </a>
          </li>
          <li>
            <a href="#">
              <img
                src="../assets/img/footer-periscope.png"
                alt="Periscope icon"
              />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mixin.scss" as *;
@use "../assets/scss/variables.scss" as *;

/**************
PARTE CENTRALE
**************/
.footer-main {
  background-image: url("../assets/img/footer-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  // debug
  height: 400px;

  .container {
    position: relative;

    display: flex;
    column-gap: 1rem;
    padding: 1rem 0;

    .my-footer-col {
      width: 10%;
      height: calc(400px - 2rem);
      display: flex;
      flex-direction: column;

      .footer-list-title {
        color: #fff;
        font-weight: bold;
        margin: 0.5rem 0;
      }

      ul {
        margin-bottom: 2rem;

        li {
          color: #999;
          font-size: 0.7rem;
          margin: 0.5rem 0;

          &:hover {
            color: #fff;
          }
        }
      }
    }

    // Logo di sfondo
    img {
      width: 45%;

      position: absolute;
      right: 0;
      top: -50px;
    }
  }
}

/***************
PARTE INFERIORE
***************/
.footer-bottom {
  height: 100px;
  background-color: #333;

  position: relative;
  z-index: 1;

  .container {
    @include flex-center();
    height: 100%;

    .outlined-btn {
      border: 2px solid #0160ba;
      background-color: #333;
      padding: 0.5rem;
      font-weight: bold;
      color: #fff;
      cursor: pointer;

      &:hover {
        background-color: #0160ba;
      }
    }

    ul {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      flex-grow: 1;
      margin-right: 0;

      li {
        margin: 0 0.5rem;

        span {
          color: $primary-color;
          font-weight: bold;
        }

        img {
          width: 2rem;
        }
      }
    }
  }
}
</style>
