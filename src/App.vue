<template>
  <div id="app">
    <div id="nav-wide" class="fixed-nav-bar">
      <nav>
        <div id="nav-content">
          <router-link to="/">HOME</router-link>
          <div class="links">
            <router-link to="/design">design</router-link>
            <router-link to="/development">development</router-link>
            <router-link to="/music">music</router-link>
          </div>
          <div class="big-wrapper" @mouseover="hover = true" @mouseleave="hover = false">
            <div class="profile">
              <img class="pic" src="https://i.imgur.com/L9rLNo7.png">
              <div class="text">Jeremy Stern</div>
              <img id="chevron" src="./assets/chevron-down.svg">
            </div>
            <!-- <contact v-if="true"></contact> -->
            <contact v-if="hover"></contact>
          </div>
        </div>
      </nav>
    </div>
    <router-view id="page-content"/>
    <hire-me-button></hire-me-button>
  </div>
</template>

<script>
import HireMeButton from "@/components/HireMeButton.vue";
import Contact from "@/components/Contact.vue";

export default {
  name: "App",
  components: {
    HireMeButton,
    Contact
  },
  data() {
    return {
      hover: false
    };
  },
  methods: {
    isHovering() {}
  }
};
</script>

<style lang="scss">
@import "/styles/global.scss";

.active {
  background: green;
}
#app {
  font-family: "Avenir Next", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  // z-index: 0;
  // overflow: hidden;
  // overflow: visible !important;
}
#page-content {
  max-width: $max-width;
  // margin: 0 $margin;
  margin: $med 10vw;
  text-align: center;
  z-index: 1;
}
#nav-wide {
  width: 500%;
  margin-left: -200%;
  border-bottom: 2px solid rgba(196, 196, 196, 0.25);
  z-index: 100;
  // overflow: visible !important;
}
#nav-content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 75vw;
}
.fixed-nav-bar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.97);
  backdrop-filter: blur(10px);
}
// nav a::after {
//   content: "";
//   background: $music-color;
//   height: 2px;
//   position: absolute;
//   bottom: 0;
//   transition: 0.16s all 0.025s;
//   // margin-bottom: -2px !important;
// }
// nav a::after {
//   left: 100%;
//   right: 0;
// }
// nav a:hover ~ a::after {
//   left: 0;
//   right: 100%;
// }
// nav a:hover::after {
//   left: 0;
//   right: 0;
// }
nav {
  display: inline-block;
  height: $navbar-height;
  line-height: $navbar-height;
  max-width: $max-width;

  .links {
    font-size: 16px;
    font-variant: small-caps;
    color: $gray;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-grow: 0.4;
  }

  a {
    @extend %quick-ease;
    position: relative;
    display: inline-block;
    color: $gray;
    &.router-link-exact-active {
      border-bottom: 2px solid $dev-color;
      color: black;

      // content: "";
      // background: $dev-color;
      // height: 2px;
      // // position: fixed;
      // // position: absolute;
      // position: relative;
      // bottom: 0;
      // transition: 0.16s all 0.025s;
      // margin-bottom: -2px !important;
      // margin-top: 90px;
    }

    &:hover {
      color: $dev-color;
      text-shadow: 2px 4px 6px rgba(0, 0, 0, 0.13);
    }
  }

  .profile {
    @extend %quick-ease;
    display: flex;
    flex-direction: row;

    .pic {
      // box-shadow: 2px 4px 7px rgba(0, 0, 0, 0.1);
      border-radius: 50%;
      width: 30px;
      height: 30px;
      margin: auto;
      padding-right: 12px;

      &:hover {
        // TODO ; add box shadow
      }
    }

    .text {
      text-transform: capitalize;
      font-weight: normal;
      font-size: 14px;
    }

    #chevron {
      margin-left: 8px;
      margin-top: 2px;
    }

    &:hover {
      cursor: pointer;
      color: $gray;
    }
  }
}
</style>
