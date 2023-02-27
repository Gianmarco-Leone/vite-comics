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
  methods: {
    changeActive(i) {
      if (this.links[i].active == false) {
        this.links[i].active = true;
      } else {
        this.links[i].active = false;
      }
    },
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="Logo" />
      <ul>
        <li v-for="(link, index) in links">
          <a
            :href="link.url"
            :class="link.active ? 'active' : ''"
            @click="changeActive(index)"
          >
            {{ link.text }}
          </a>
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
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: flex-end;
      flex-grow: 1;
      margin-right: 0;

      li {
        margin: 0 0.5rem;
        font-weight: 600;
        font-size: 0.8rem;

        a {
          display: inline-block;
          height: 100px;
          line-height: 100px;
        }

        .active {
          color: #0282f9;
          border-bottom: 5px solid #0282f9;
        }
      }
    }
  }
}
</style>
