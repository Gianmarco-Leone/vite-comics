<script>
// Importo componente fascia azzurra
import AppFooterTop from "./AppFooterTop.vue";

export default {
  // Recupero la lista dei menu del footer
  props: {
    menus: Array,
  },
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
        <!-- Singola colonna -->
        <div v-for="menu in menus" class="my-footer-col">
          <span class="footer-list-title">
            {{ menu.title }}
          </span>
          <ul>
            <li v-for="link in menu.links">
              <a :href="link.url">
                {{ link.text }}
              </a>
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
    height: 100%;
    position: relative;

    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-content: flex-start;
    column-gap: 1rem;
    padding: 1rem 0;

    .my-footer-col {
      width: 10%;
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
