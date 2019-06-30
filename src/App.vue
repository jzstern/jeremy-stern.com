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
              <img class="pic" src="https://i.imgur.com/L9rLNo7.png" />
              <div class="text">Jeremy Stern</div>
              <img id="chevron" src="./assets/chevron-down.svg" />
            </div>
            <transition name="slide-fade">
              <!-- <contact v-if="true"></contact> -->
              <contact v-if="hover"></contact>
            </transition>
          </div>
        </div>
      </nav>
    </div>
    <router-view id="page-content" />
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

.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  // transition: all 0.5s cubic-bezier(1, 0.9, 0.1, 1);
  transition: all 0.5s ease;
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(10px);
  // transform: rotateY(50deg);
  opacity: 0;
}

body {
  // background: linear-gradient(
  //   158.73deg,
  //   #038194 0%,
  //   #26a699 26.04%,
  //   #038194 26.05%,
  //   #03343b 64.06%,
  //   rgba(3, 129, 148, 1) 64.06%
  // );
  background: linear-gradient(
    158.73deg,
    #038194 0%,
    #26a699 26.04%,
    #038194 26.05%,
    #03343b 64.06%,
    rgba(3, 129, 148, 0.359375) 64.06%,
    #3a5c7e 64.07%,
    rgba(58, 92, 126, 0.61) 100%
  );
}

.active {
  background: green;
}
#app {
  font-family: "Avenir Next", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  position: relative;
  // z-index: 0;
  // overflow: hidden;
  // overflow: visible !important;
}
#page-content {
  max-width: $max-width;
  margin: auto;
  margin-top: $med !important;
  margin-bottom: $med !important;
  text-align: center;
  z-index: 1;
  color: white;

  a {
    color: #b0d2d9;
    &:hover {
      color: $design-color;
    }
  }
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
#nav-wide {
  width: 500%;
  margin-left: -200%;
  // border-bottom: 2px solid white; // TODO ; decide about this line
  // border-bottom: 2px solid rgba(196, 196, 196, 0.25); // TODO ; decide about this line
  z-index: 100;
  // overflow: visible !important;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
}
.fixed-nav-bar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.97);
}
nav {
  display: inline-block;
  height: $navbar-height;
  line-height: $navbar-height;
  max-width: $max-width;

  #nav-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 75vw;
  }

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
      border-bottom: 4px solid $dev-color;
      color: black;

      // content: "";
      // background: $dev-color;
      height: 0px;
      // // position: fixed;
      // // position: absolute;
      // position: relative;
      // bottom: 0;
      // transition: 0.16s all 0.025s;
      // margin-bottom: -2px !important;
      // margin-top: $navbar-height;
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
