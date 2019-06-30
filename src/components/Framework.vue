<template>
  <div class="bubble">{{ title }}</div>
</template>

<script>
export default {
  name: "Framework",
  props: ["title"]
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";
.bubble {
  @extend %quick-ease;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  color: #e4e4e4;
  border: 1px solid#e4e4e4;
  box-sizing: border-box;
  border-radius: 15px;
  width: 105px;
  height: 30px;
  margin-bottom: $base;

  &:hover {
    cursor: default;
    color: white;
    border-color: white;
    box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.13);
  }
}
// .bubble-old {
//   @extend %quick-ease;
//   display: flex;
//   flex-direction: column;
//   justify-content: center;
//   text-align: center;
//   color: $gray;
//   border: 1px solid $gray;
//   box-sizing: border-box;
//   border-radius: 15px;
//   width: 105px;
//   height: 30px;
//   margin-bottom: $base;

//   &:hover {
//     cursor: pointer;
//     color: $dev-color;
//     border-color: $dev-color;
//     // box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
//     box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.13);
//   }
// }
</style>
