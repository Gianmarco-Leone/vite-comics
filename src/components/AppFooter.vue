<script>
export default {};
</script>

<template>
  <footer>
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
    <div class="footer-bottom"></div>
  </footer>
</template>

<style lang="scss" scoped>
// Parte centrale footer
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

// Parte inferiore Footer
.footer-bottom {
  height: 100px;
  background-color: #444;

  position: relative;
  z-index: 1;
}
</style>
