<template>
  <div class="design-preview">
    <h3>{{ title }}</h3>
    <p>{{ text }}</p>
    <br>
    <a :href="url" target="_blank">
      <img :src="previewUrl">
    </a>
  </div>
</template>

<script>
export default {
  name: "DesignPreview",
  props: {
    title: String,
    text: String,
    previewUrl: String,
    url: String
  }
};
</script>

<style scoped lang="scss">
@import "../styles/global.scss";
$preview-width: $lg * 4;
$preview-height: $lg * 2;

.design-preview {
  //   margin: $sm 0;
  //   text-align: left;
  text-align: center;
  p {
    font-size: 16px;
    text-align: left;
  }

  h3 {
    text-align: left;
  }

  a {
    @extend %quick-ease;
    display: inline-block;
    margin-bottom: $sm;
    border: 1px solid rgba(0, 0, 0, 0.3);

    img {
      max-width: 100%;
      vertical-align: top;

      //   @if (this.title != "Rocky Road") {
      //   }
    }

    &:hover {
      box-shadow: 2px 4px 15px rgba(0, 0, 0, 0.3);
    }
  }
}
</style>
