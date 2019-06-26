<template>
  <div class="contact">
    <div class="spacing">
      <!-- <social name="Twitter" url="https://twitter.com/jzstern" iconPath="../assets/twitter.svg"></social> -->
      <p>Want to get in touch?</p>
      <div class="socials">
        <social
          v-for="item in socialData"
          :key="item.name"
          :name="item.name"
          :url="item.url"
          :iconPath="item.iconPath"
        ></social>
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

  data: function() {
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
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";
.contact {
  @extend %quick-ease;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  color: $gray;
  box-sizing: border-box;
  border-radius: 12px;
  box-shadow: 3px 4px 15px rgba(0, 0, 0, 0.3);
  width: 330px;
  height: 210px;
  //   margin: $sm;

  //   &:hover {
  //     cursor: pointer;
  //     color: $dev-color;
  //     border-color: $dev-color;
  //     // box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  //     box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.13);
  //   }
}

.spacing {
  padding: $base;
}
</style>
