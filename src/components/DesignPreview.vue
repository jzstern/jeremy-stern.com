<template>
  <div class="design-preview">
    <h3>{{ title }}</h3>
    <p>{{ text }}</p>
    <br />
    <carousel class="pics" :data="slides" indicators="hover" :autoplay="false"></carousel>
  </div>
</template>

<script>
import VueCarousel from "@chenfengyuan/vue-carousel";
export default {
  name: "DesignPreview",
  components: {
    VueCarousel
  },
  props: {
    title: String,
    text: String,
    slides: Array
  }
};
</script>

<style scoped lang="scss">
@import "../styles/global.scss";
$preview-width: $lg * 4;
$preview-height: $lg * 2;

.design-preview {
  text-align: center;
  p {
    font-size: 16px;
    text-align: left;
  }

  h3 {
    text-align: left;
  }
}

.pics {
  //   border: 1px solid $gray;
  margin-bottom: $sm;
  line-height: 0px;
  box-shadow: 2px 4px 15px rgba(0, 0, 0, 0.3);
}
</style>
