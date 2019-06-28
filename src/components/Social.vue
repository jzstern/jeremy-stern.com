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
  line-height: 0 !important;
  // height: 1rem;

  a {
    @extend %quick-ease;
    color: $gray;
    position: relative;
    align-items: center;
    height: 25px;
    display: flex;
    flex-direction: row;
    &:hover {
      color: black;
    }

    p {
      font-size: 16px;
    }
    img {
      margin-right: 8px;
    }
  }
}
</style>
