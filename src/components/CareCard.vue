<template>
  <div class="care-card">
    <img :src="this.getPath(iconPath)" />
    <h3>{{ title }}</h3>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "CareCard",
  props: {
    iconPath: String,
    title: String,
    text: String
  },
  methods: {
    getPath(iconPath) {
      return require("../assets/" + iconPath);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/global.scss";

$card-width: 300px;
$card-height: 300px;
$card-padding: $base * 2;

.care-card {
  @extend %quick-ease;
  width: $card-width - $card-padding;
  height: $card-height - $card-padding;
  background-color: rgba(255, 255, 255, 0.9);
  // max-width: $card-width;
  // max-height: $card-height;
  box-shadow: 2px 4px 15px rgba(0, 0, 0, 0.3);
  padding: $card-padding;
  margin: $base;
  border-radius: $corner;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-content: space-between;

  &:hover {
    box-shadow: 6px 10px 12px rgba(0, 0, 0, 0.5);
    background: white;
  }

  img {
    margin-top: $base;
    margin-bottom: $base * 2;
  }

  h3 {
    margin: 0;
    color: $primary-color;
  }

  p {
    font-weight: normal;
    font-size: 18px;
    flex-grow: 2;
    color: black;
  }
}
</style>
