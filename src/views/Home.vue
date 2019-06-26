<template>
  <div class="home">
    <p id="hi">Hi, my name is</p>
    <h1 id="me">Jeremy Stern</h1>

    <p id="ima">
      I'm a
      <router-link to="/design">
        <strong class="design">Product Designer</strong>
      </router-link>,
      <router-link to="/development">
        <strong class="dev">Developer</strong>
      </router-link>, and
      <router-link to="/music">
        <strong class="music">Sound Wizard</strong>
      </router-link>
    </p>

    <div id="scroll">vvvvvvv</div>

    <div class="row">
      <Card
        type="design"
        :title="this.designTitle"
        :text="this.designText"
        :button="this.designButton"
      />
      <span>
        <img src="../assets/layout.svg">
      </span>
    </div>

    <div class="row">
      <span>
        <img src="../assets/code.svg">
      </span>
      <Card
        type="development"
        :title="this.devTitle"
        :text="this.devText"
        :button="this.devButton"
      />
    </div>

    <div class="row">
      <Card
        type="music"
        :title="this.musicTitle"
        :text="this.musicText"
        :button="this.musicButton"
      />
      <span>
        <img src="../assets/headphones.svg">
      </span>
    </div>

    <div class="spacer"></div>

    <h4>I care about</h4>
    <div class="care-container">
      <span class="care">
        <img src="../assets/users.svg">
        <p class="text2">People</p>
        <p>{{ people }}</p>
      </span>
      <span class="care">
        <img src="../assets/lock.svg">
        <p class="text2">Privacy</p>
        <p>{{ privacy }}</p>
      </span>
      <span class="care">
        <img src="../assets/sun.svg">
        <p class="text2">Nature</p>
        <p>{{ nature }}</p>
      </span>
    </div>

    <div class="spacer"></div>

    <p>When I’m not busy with any of the former, you’ll find me doing any of the following</p>
    <div class="interests">
      <p>
        Skiing
        <br>Photography
        <br>Climbing
      </p>
      <p>
        Reading
        <br>Surfing
        <br>Exploring
      </p>
      <p>
        Hiking
        <br>Learning
        <br>SCUBA
      </p>
      <p>
        Cooking
        <br>Paintballing
        <br>Barbacking
      </p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Card from "@/components/Card.vue";

export default {
  name: "home",
  components: {
    Card
  },
  data() {
    return {
      designTitle: "I practice human-centered design",
      designText:
        "Why shouldn’t every website be grandma friendly? I get users from point A to Z without any friction. No ambiguities. No bloatware. Clean & simple.",
      designButton: "check out my work",
      devTitle: "I'm an agile developer",
      devText:
        "I make stuff... and break stuff! I’ve studied everything from Object-Oriented Design to Artificial Intelligence. I’m familiar with a handful of frameworks and I’m always looking for new ways to do things.",
      devButton: "see what i'm building",
      web3Title: "I'm passionate about decentralization",
      web3Text:
        "We are witnessing the reinvention of value exchange, network protocol design, and so much more! Cryptocurrency and Web 3 has the power to disrupt every industry, and I can’t wait to see what the future holds for distributed computing.",
      web3Button: "view my crypto projects",
      musicTitle: "I live for music",
      musicText:
        "Whether it’s producing, djing, playing bass guitar, making weird noises, tinkering with hardware, mixing/mastering or even just listening... I can’t go one day without some kind of auditory stimulation.",
      musicButton: "listen to my sounds",
      people:
        "I love hearing stories, perspectives, and interests from those who are different from me",
      privacy:
        "We leave digital traces of ourselves everywhere, all the time. This data should not be available to onlookers",
      nature:
        "There’s only one earth, and it’s a pretty good one. I want to leave this planet better than I found it"
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";
.row {
  position: relative;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  // justify-content: space-around;
  // justify-content: space-evenly;
  flex-basis: min-content;
  vertical-align: middle;
}
#hi {
  // padding-top: $sm * 3;
  animation: fadein 2s;
}
#me {
  animation: fadein 4s;
}
#ima {
  padding: $med 0;
  // padding: $med 0;
  animation: fadein 6s;
  display: inline-block;
}
#scroll {
  padding-bottom: $med;
  animation: fadein 10s;
}
.design:hover {
  color: $design-color;
}
.dev:hover {
  color: $dev-color;
}
.music:hover {
  color: $music-color;
}
strong {
  font-weight: 600;
  color: black;
  @extend %quick-ease;
}
.care-container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;

  .text2 {
    font-weight: 500;
  }
}
.care {
  width: $lg;
}
.interests {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;

  p {
    text-align: left;
    color: #6f6f6f;
  }
}
@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
.home {
  padding-top: $sm * 3;
}
</style>
