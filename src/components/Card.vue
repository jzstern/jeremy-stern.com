<template>
  <div class="card">
    <h3>{{ title }}</h3>
    <p>{{ text }}</p>
    <div class="card-btn">
      <router-link :to="'/' + type" class="card-btn">{{ button }}</router-link>
      <!-- <router-link :to="'/' + type">{{ button }}</router-link> -->
    </div>
    <!-- <div class="shadow">lol</div> -->
  </div>
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
$card-padding: 30px;

.card {
  border: 1px black;
  width: $card-width - $card-padding;
  height: $card-height - $card-padding;
  // max-width: $card-width;
  // max-height: $card-height;
  box-shadow: 2px 4px 15px rgba(0, 0, 0, 0.3);
  padding: $card-padding;
  margin: 30px;
  border-radius: 12px;
  text-align: left;
  display: flex;
  flex-direction: column;
  align-content: space-between;
}
p {
  font-weight: normal;
  font-size: 14px;
  line-height: 19px;
  flex-grow: 2;
}

// TODO ; add fade in to cards
.card-btn {
  color: $card-btn-text-color;
  font-weight: 600;
  font-size: 18px;
  font-variant: small-caps;
  // position: absolute;
  // bottom: 0;
  width: 100%;

  &:hover {
    color: $card-btn-highlight-color;
  }
}
</style>
