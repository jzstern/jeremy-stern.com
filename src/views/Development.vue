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
      <h2>Loft Radio</h2>
      <p>I'm currently chugging away on a project called Loft; a 24/7 music stream that enables listeners to tip artists in small amounts of cryptocurrency. Experimenting with new ways of fostering community engagement, exchanging value between artists and listeners, and playful interactions.</p>
      <p>See this Twitter thread for more info and don't hesitate to reach out if you're curious!</p>
      <br>
      <br>
      <h2>Web 3 & Cryptocurrency</h2>
      <p>I'm very passionate about the decentralized web and the potential of blockchain technology. We are currently witnessing the reinvention of value exchange, network protocol design, and so much more! Cryptocurrency and Web 3 has the power to disrupt every industry, and I can’t wait to see what the future holds for distributed computing.</p>
      <br>
      <br>
      <p>More coming soon...</p>
      <br>
      <p>
        In the meantime, feel free to check out my
        <a href="https://github.com/jzstern/">Github</a>,
        <a href="https://i.imgur.com/2zCvnOj.jpg">resume</a>, or even the
        <a href="https://github.com/jzstern/jeremy-stern.com">source code</a> for this site if you're curious!
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

a {
  @extend %quick-ease;
  color: $dev-color;

  &:hover {
    color: $design-color;
  }
}
</style>
