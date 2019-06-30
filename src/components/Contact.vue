<template>
  <div id="wrapper">
    <div class="contact">
      <div class="spacing">
        <!-- <social name="Twitter" url="https://twitter.com/jzstern" iconPath="../assets/twitter.svg"></social> -->
        <p class="title">Want to get in touch?</p>
        <div class="socials">
          <social
            v-for="item in socialData"
            :key="item.name"
            :name="item.name"
            :url="item.url"
            :iconPath="item.iconPath"
          ></social>
          <!-- <div class="night-mode-switch">
          <img src="../assets/moon.svg"/>>
          click me
          </div>-->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Social from "../components/Social.vue";
export default {
  name: "Contact",
  components: {
    Social
  },

  data() {
    return {
      socialData: [
        {
          name: "Email",
          url: "mailto:jzstern@gmail.com",
          iconPath: "email.svg"
        },
        {
          name: "Twitter",
          url: "https://twitter.com/jzstern",
          iconPath: "twitter.svg"
        },
        {
          name: "Instagram",
          url: "https://www.instagram.com/jzstern/",
          iconPath: "instagram.svg"
        },
        // {
        //   name: "Soundcloud",
        //   url: "https://soundcloud.com/palmingo",
        //   iconPath: "soundcloud.svg"
        // },
        {
          name: "Dribbble",
          url: "https://dribbble.com/jzstern",
          iconPath: "dribbble.svg"
        },
        {
          name: "Github",
          url: "https://github.com/jzstern/",
          iconPath: "github.svg"
        },
        {
          name: "LinkedIn",
          url: "https://www.linkedin.com/in/jeremy-stern-6a5a2490/",
          iconPath: "linkedin.svg"
        },
        {
          name: "Soundcloud",
          url: "https://soundcloud.com/palmingo",
          iconPath: "soundcloud.svg"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";
#wrapper {
  width: 100%;
  position: fixed;
  display: inline-block;
  text-align: right;
  z-index: 999999;
  line-height: 1pt !important;
  margin-top: -$base * 1.5;
  margin-left: -$med;
}
.contact {
  @extend %quick-ease;
  position: fixed;
  display: flex;
  flex-direction: column;
  justify-content: center;
  box-sizing: border-box;
  border-radius: $corner;
  background: white;
  box-shadow: 3px 4px 15px rgba(0, 0, 0, 0.3);
  width: $lg - $base * 2;
  height: 230px;

  //   &:hover {
  //     cursor: pointer;
  //     color: $dev-color;
  //     border-color: $dev-color;
  //     // box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  //     box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.13);
  //   }
}

.title {
  margin-top: 1;
  text-align: left;
}

.night-mode-switch {
  @extend %quick-ease;
  border: 1px solid #cccccc;
  box-sizing: border-box;
  // border-radius: 15px;
  width: 88px;
  height: 32px;
  font-variant: small-caps;
  font-size: 12px;
  color: $gray;

  &:hover {
    color: black;
    cursor: pointer;
    border-color: black;
  }
}

.spacing {
  padding: $base;
  // max-height: 210px;
  // height: 210px;
}
</style>
