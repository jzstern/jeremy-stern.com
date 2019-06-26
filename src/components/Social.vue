<template>
  <div class="social">
    <a :href="url" target="_blank">
      <img :src="this.getPath(iconPath)">
      <p>{{ name }}</p>
      <!-- <a :href="url" target="_blank">{{ name }}</a> -->
    </a>
  </div>
</template>

<script>
export default {
  name: "Social",
  props: ["name", "url", "iconPath"],
  methods: {
    getPath(iconPath) {
      // TODO ; change shade of icon upon hover
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
  margin-top: 11px; // TODO ; fix this goddam alignment bug.
  // line-height: 0 !important;
  // line-height: 0.1pt !important;
  // line-height: 0.1pt !important;
  // max-height: 15px;
  // height: 1rem;

  a {
    @extend %quick-ease;
    color: $gray;
    vertical-align: center; // TODO ; comment out these two vvvvvvvv
    display: inline-block;
    // position: relative;
    // margin: auto;
    // display: flex;  // TODO ; add these two lines back in vvvvvvvv
    // flex-direction: row;
    &:hover {
      color: black;
    }
  }

  p {
    display: inline;
    // vertical-align: center;
    font-size: 16px;
  }

  img {
    // margin: auto;
    margin-right: 8px;
    // vertical-align: center;
    // position: relative;
  }
}
</style>
