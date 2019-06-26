<template>
  <div class="social">
    <!-- <img :src="iconPath"> -->
    <!-- <img :src="'~assets/' + iconPath"> -->
    <img :src="this.getPath(iconPath)">
    <a :href="url" target="_blank">{{ name }}</a>
  </div>
</template>

<script>
export default {
  name: "Social",
  props: ["name", "url", "iconPath"],
  methods: {
    getPath(iconPath) {
      return require("../assets/" + iconPath);
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";
.social {
  @extend %quick-ease;
  display: flex;
  flex-direction: row;
  //   justify-content: center;
  //   text-align: center;

  a {
    @extend %quick-ease;
    color: $gray;
    &:hover {
      color: black;
    }
  }

  img {
    margin-right: 8px;
  }
}
</style>
