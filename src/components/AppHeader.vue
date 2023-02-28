<script>
export default {
  props: {
    listLinks: Array,
  },

  // methods: {
  //   changeActive(i) {
  //     if (this.links[i].active == false) {
  //       this.links[i].active = true;
  //     } else {
  //       this.links[i].active = false;
  //     }
  //   },
  // },
};
</script>

<template>
  <header>
    <div class="container">
      <a href="#">
        <img src="../assets/img/dc-logo.png" alt="Logo" />
      </a>
      <ul>
        <li v-for="(link, index) in listLinks" :key="link.text">
          <a :href="link.url" :class="link.active ? 'active' : ''">
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
          color: #444;
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
