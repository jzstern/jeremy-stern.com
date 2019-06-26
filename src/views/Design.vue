<template>
  <div class="design">
    <!-- <h1>Design</h1> -->
    <contact></contact>
    <p class="floater">
      I use Figma
      <br>Less is more
      <br>Night mode 2020
    </p>
  </div>
</template>

<script>
import Contact from "../components/Contact.vue";
export default {
  name: "Design",
  components: {
    Contact
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";
</style>
