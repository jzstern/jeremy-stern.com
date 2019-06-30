<template>
  <router-link :to="'/' + type">
    <div class="card">
      <h3>{{ title }}</h3>
      <p>{{ text }}</p>
      <div class="card-btn">
        <router-link :to="'/' + type" class="card-btn">{{ button }}</router-link>
      </div>
      <!-- <div class="shadow">lol</div> -->
    </div>
  </router-link>
</template>

<script>
export default {
  name: "Card",
  props: {
    type: String,
    title: String,
    text: String,
    button: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/global.scss";

$card-btn-text-color: #038194;
$card-btn-highlight-color: #78a93b;
$card-width: 390px;
$card-height: 240px;
$card-padding: $base * 2;

.card {
  @extend %quick-ease;
  backdrop-filter: blur(10px);
  color: black !important;
  width: $card-width - $card-padding;
  height: $card-height - $card-padding;
  background-color: rgba(255, 255, 255, 0.9);
  // max-width: $card-width;
  // max-height: $card-height;
  box-shadow: 2px 4px 15px rgba(0, 0, 0, 0.3);
  padding: $card-padding;
  margin: $med;
  border-radius: $corner;
  text-align: left;
  display: flex;
  flex-direction: column;
  align-content: space-between;

  &:hover {
    background-color: white !important;
    box-shadow: 6px 10px 12px rgba(0, 0, 0, 0.5);

    .card-btn {
      color: $design-color !important;
      // color: #04444d !important;
    }
  }

  h3 {
    margin: 0;
  }

  p {
    font-weight: normal;
    font-size: 16px;
    flex-grow: 2;
  }
  // TODO ; add fade in to cards
  .card-btn {
    @extend %quick-ease;
    color: $card-btn-text-color !important;
    font-weight: 600;
    font-size: 18px;
    font-variant: small-caps;

    // &:hover {
    //   // color: $card-btn-highlight-color !important;
    //   color: #04444d !important;
    //   // color: $design-color !important;
    // }
  }
}
</style>
