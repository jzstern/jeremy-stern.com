<template>
  <div
    class="wrapper"
    data-aos="fade-up"
    data-aos-anchor-placement="top-bottom"
    data-aos-duration="1200"
    data-aos-easing="ease"
  >
    <img src="../assets/briefcase-white.svg" />
    <h4 style="font-size: 16px; font-weight: 500; color: white;">Currently available for hire</h4>
    <div
      id="hire-me"
      class="box-shadow-transition box-shadow-below box-shadow-below-hover"
      onclick="location.href='mailto:jzstern@gmail.com';"
      data-aos-delay="1200"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
    >
      <div id="butt">
        <p>Email me for inquires</p>
        <img src="../assets/send.svg" style="filter: invert(100%); margin-left: 8px;" />
      </div>
    </div>
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
AOS.init({ once: true });

export default {
  name: "HireMeButton"
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";
$aos-distance: $base * 2; // It has to be above import
@import "node_modules/aos/src/sass/aos.scss";

h4 {
  margin-bottom: $sm / 2;
}

.wrapper {
  margin-bottom: $sm;
}

#hire-me {
  @extend %quick-ease;
  color: white;
  width: $lg + $base;
  height: $sm;
  background: #209d98;
  border-radius: 50px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-size: 12px;
  margin: auto;
  box-shadow: 1px 4px 12px rgba(0, 0, 0, 0.3);

  &:hover {
    box-shadow: 2px 8px 12px rgba(0, 0, 0, 0.5);
    cursor: pointer;
    // -webkit-box-shadow: 6px 16px 18px -6px rgba(0, 0, 0, 0.3);
    // -moz-box-shadow: 6px 12px 18px -6px rgba(0, 0, 0, 0.3);
    // box-shadow: 6px 12px 18px -6px rgba(0, 0, 0, 0.3);
  }

  div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: auto;
  }

  #butt {
    flex-direction: row;
    justify-content: space-between;
  }
}

// .box-shadow-transition {
//   -webkit-transition: all 0.3s ease-in-out;
//   -moz-transition: all 0.3s ease-in-out;
//   -ms-transition: all 0.3s ease-in-out;
//   -o-transition: all 0.3s ease-in-out;
// }
// .box-shadow-below {
//   -webkit-box-shadow: 2px 8px 12px -6px rgba(0, 0, 0, 0.75);
//   -moz-box-shadow: 2px 8px 12px -6px rgba(0, 0, 0, 0.75);
//   box-shadow: 2px 8px 12px -6px rgba(0, 0, 0, 0.75);
// }
// .box-shadow-below-hover:hover {
//   -webkit-box-shadow: 0 12px 18px -6px black;
//   -moz-box-shadow: 0 12px 18px -6px black;
//   box-shadow: 0 12px 18px -6px black;
// }
</style>
