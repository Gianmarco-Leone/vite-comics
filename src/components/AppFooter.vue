<script>
export default {};
</script>

<template>
  <footer>
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

    <!-- Parte centrale Footer -->
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

    <!-- Parte inferiore Footer -->
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

/**************
PARTE SUPERIOE
**************/
.footer-top {
  height: 150px;
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
          color: #0282f9;
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
