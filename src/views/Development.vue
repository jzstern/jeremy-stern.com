<template>
  <div id="dev">
    <!-- <h1>Development</h1> -->
    <p class="floater">The more I learn, the more I realize I don't know</p>
    <div class="content">
      <h2>Frameworks & Languages</h2>
      <div class="frameworks">
        <framework v-for="name in frameworks" :key="name" :title="name"></framework>
      </div>

      <i>I also have experience with Node, MongoDB, AWS Amplify, web3, IPFS, React Native, jQuery, Bootstrap, Material, C++ and more (:</i>
      <br>
      <br>
      <p>Busy chugging away on a project called Loft Radio; a 24/7 music stream that enables listeners to tip artists in small amounts of cryptocurrency. Experimenting with new ways of fostering community engagement, exchanging value between artists and listeners, and playful interactions.</p>
      <br>
      <p>More coming soon...</p>
      <br>
      <p>
        In the meantime, feel free to check out my
        <a href="https://github.com/jzstern/">Github</a> or my
        <a href="https://i.imgur.com/2zCvnOj.jpg">resume</a>, or even the source code for this site if you're curious!
      </p>
    </div>
  </div>
</template>

<script>
import Framework from "../components/Framework.vue";
export default {
  name: "Development",
  components: {
    Framework
  },
  data: function() {
    return {
      frameworks: [
        "React",
        "Vue",
        "Angular",
        "SQL",
        "GraphQL",
        "Redux",
        "Vuex",
        "ES6",
        "Java",
        "Python"
      ]
    };
  }
};
</script>

<style scoped lang="scss">
@import "../styles/global.scss";

#dev {
  text-align: center;
}

.content {
  display: inline-block;
  text-align: left;
  width: $med * 5;
  // max-width: $med * 5;
}

.frameworks {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-bottom: $base;
}
</style>
