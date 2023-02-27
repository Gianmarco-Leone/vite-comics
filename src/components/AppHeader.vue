<script>
export default {
  data() {
    return {
      //   logo: "../assets/img/dc-logo.png",
      links: [
        {
          text: "CHARACTERS",
          url: "#",
          active: false,
        },
        {
          text: "COMICS",
          url: "#",
          active: false,
        },
        {
          text: "MOVIES",
          url: "#",
          active: false,
        },
        {
          text: "TV",
          url: "#",
          active: false,
        },
        {
          text: "GAMES",
          url: "#",
          active: false,
        },
        {
          text: "COLLECTIBLES",
          url: "#",
          active: false,
        },
        {
          text: "VIDEOS",
          url: "#",
          active: false,
        },
        {
          text: "FANS",
          url: "#",
          active: false,
        },
        {
          text: "NEWS",
          url: "#",
          active: false,
        },
        {
          text: "SHOP",
          url: "#",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="Logo" />
      <ul>
        <li v-for="link in links">
          {{ link.text }}
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mixin.scss" as *;

header {
  background-color: #fefefe;
  height: 100px;

  .container {
    @include flex-center();
    height: 100%;

    img {
      height: 70px;
    }

    ul {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      flex-grow: 1;
      margin-right: 0;

      li {
        margin: 0 0.5rem;
        font-weight: 600;
        font-size: 0.8rem;
      }
    }
  }
}
</style>
