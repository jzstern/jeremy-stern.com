<template>
  <div class="wrapper">
    <h4 style="font-size: 16px; font-weight: 600">Currently available for hire</h4>
    <div
      id="hire-me"
      class="box-shadow-transition box-shadow-below box-shadow-below-hover"
      onclick="location.href='mailto:jzstern@gmail.com';"
    >
      <span>
        <!-- <img src="../assets/briefcase-white.svg"> -->
        <img src="../assets/briefcase.svg">
      </span>
      <p>Email me for inquires</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HireMeButton"
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";

h4 {
  margin-bottom: $sm / 2;
}

.wrapper {
  margin-bottom: $sm;
}

#hire-me {
  width: 270px;
  height: 210px;
  // background: $music-color;
  background: #75bac4;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-size: 12px;
  margin: auto;

  &:hover {
    cursor: pointer;
    // -webkit-box-shadow: 6px 16px 18px -6px rgba(0, 0, 0, 0.3);
    // -moz-box-shadow: 6px 12px 18px -6px rgba(0, 0, 0, 0.3);
    // box-shadow: 6px 12px 18px -6px rgba(0, 0, 0, 0.3);
  }
}

.box-shadow-transition {
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -ms-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
}
.box-shadow-below {
  -webkit-box-shadow: 0 8px 12px -6px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 0 8px 12px -6px rgba(0, 0, 0, 0.75);
  box-shadow: 0 8px 12px -6px rgba(0, 0, 0, 0.75);
}
.box-shadow-below-hover:hover {
  -webkit-box-shadow: 0 12px 18px -6px black;
  -moz-box-shadow: 0 12px 18px -6px black;
  box-shadow: 0 12px 18px -6px black;
}
</style>
