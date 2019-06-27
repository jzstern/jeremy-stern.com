<template>
  <div class="design">
    <div class="content">
      <h2 id="portfolio">
        <a href="https://dribbble.com/jzstern" target="_blank">Portfolio</a>
      </h2>
      <!-- <i>I primarily use Figma, but have experience with Sketch</i> -->
      <!-- <p>Below are a handful of projects I've worked on for hackathons, design challenges, and just for fun. Hit me up if you'd like to learn a bit more about my process!</p> -->

      <div id="images">
        <design-preview
          v-for="item in previews"
          :key="item.title"
          :title="item.title"
          :text="item.text"
          :slides="item.slides"
        ></design-preview>
      </div>
      <br>
      <!-- <h2>Philosophy</h2> -->
      <!-- <i>“People ignore design that ignores people.” - Frank Chimero</i> -->
      <i style="font-size: 20px">“People ignore design that ignores people”</i>
      <p style="font-size: 18px">- Frank Chimero</p>
      <!-- <p>Design is one of the most important yet overlooked foundations of digital products. No matter how much high level utility a service provides, user experience will make or break a product.</p>
      <p>Together, we can bring ideas to their full potential. Everything starts with defining the problem. It's not just the how, but also the why.</p>
      <p>Less is more.</p>-->
    </div>
  </div>
</template>

<script>
import DesignPreview from "../components/DesignPreview.vue";
export default {
  name: "Design",
  components: {
    DesignPreview
  },
  data() {
    return {
      previews: [
        {
          title: "Lightning Network App Store",
          text:
            "I was given a loose list of requirements to make a catalog for applications that use the Bitcoin Lightning Network. After asking questions and reshaping the requirements to support the main value propositions, I spent the day moving from low fidelity wireframes to the prototype shown below.",
          slides: [
            '<img width="600px" src="https://i.imgur.com/Q3l9rKQ.png">',
            '<img width="600px" src="https://i.imgur.com/PgqWvQk.png">',
            '<img width="600px" src="https://i.imgur.com/0mwIZwb.png">',
            '<img width="600px" src="https://i.imgur.com/WgSBziG.png">'
          ]
        },
        {
          title: "Flight Fund",
          text:
            "I snuck into ETH Denver for a day and collaborated with my friend's hackathon team to design their project's interface. Worked with the group to establish scope, user flows, required information & more before cranking these out just in time to be presented in the social impact category.",
          slides: [
            '<img width="600px" src="https://i.imgur.com/BDqeB7K.jpg">',
            '<img width="600px" src="https://i.imgur.com/HCMAPOe.jpg">',
            '<img width="600px" src="https://i.imgur.com/jv0jCE6.jpg">',
            '<img width="600px" src="https://i.imgur.com/kn2TRzi.jpg">',
            '<img width="600px" src="https://i.imgur.com/jgrXtOt.jpg">',
            '<img width="600px" src="https://i.imgur.com/CkOOVKm.jpg">',
            '<img width="600px" src="https://i.imgur.com/fgyYLa1.jpg">',
            '<img width="600px" src="https://i.imgur.com/xiKlJsg.jpg">',
            '<img width="600px" src="https://i.imgur.com/7S2eK1m.jpg">'
          ]
        },
        {
          title: "Rocky Road",
          text:
            "Concept I made for a ski/snowboard ride share app that would connect drivers with extra space in their car to people that need a cheap lift up. Spending a powder-filled winter in Denver without a car was a trying time for me, and I challenged myself to think of a simple alternative to the expensive and tedious commute options to the slopes.",
          slides: [
            '<img width="600px" src="https://i.imgur.com/j0eOX39.png">',
            '<img width="600px" src="https://i.imgur.com/iConn4U.png">',
            '<img width="600px" src="https://i.imgur.com/GlCTue9.png">',
            '<img width="600px" src="https://i.imgur.com/dX56nZW.png">',
            '<img width="600px" src="https://i.imgur.com/zWeG5Vn.png">',
            '<img width="600px" src="https://i.imgur.com/OSDX30a.png">'
          ]
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";

.content {
  display: inline-block;
  text-align: left;
  width: $med * 5;
  // max-width: $med * 5;
}

a {
  @extend %quick-ease;
  color: black;

  &:hover {
    color: $design-color;
  }
}

#images {
  text-align: center;
}
</style>
