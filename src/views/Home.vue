<template>
  <div class="home">
    <p id="hi">Hi, my name is</p>
    <h1
      id="me"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="1200"
      data-aos-delay="500"
      data-aos-easing="ease"
    >Jeremy Stern</h1>
    <p
      id="ima"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
      data-aos-delay="2000"
      data-aos-easing="ease"
    >
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

    <br />
    <img
      style="filter: invert(100%)"
      id="scroll"
      src="http://albara.org/images/6576638-0-scrolldown-black.gif?crc=4181211743"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="3000"
      data-aos-delay="3000"
    />
    <div
      class="row"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
    >
      <Card
        type="design"
        :title="this.designTitle"
        :text="this.designText"
        :button="this.designButton"
      />
      <span>
        <img src="../assets/layout-white-shadow.svg" />
      </span>
    </div>

    <div
      class="row"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
    >
      <Card
        type="development"
        :title="this.devTitle"
        :text="this.devText"
        :button="this.devButton"
      />
      <span>
        <img src="../assets/code-white-shadow.svg" />
      </span>
    </div>

    <div
      class="row"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
    >
      <Card
        type="music"
        :title="this.musicTitle"
        :text="this.musicText"
        :button="this.musicButton"
      />
      <span>
        <img src="../assets/headphones-white-shadow.svg" />
      </span>
    </div>

    <div class="spacer"></div>

    <h4
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
    >I care about</h4>
    <br />
    <br />
    <div
      class="care-container"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2500"
      data-aos-delay="300"
    >
      <CareCard
        title="People"
        text="I love hearing stories, perspectives, and interests from those who are different from me."
        iconPath="users.svg"
      />
      <CareCard
        title="Privacy"
        text="We leave digital traces of ourselves everywhere, all the time. This data should not be available to onlookers."
        iconPath="lock.svg"
      />
      <CareCard
        title="Nature"
        text="There’s only one earth, and it’s a pretty good one. I want to leave this planet better than I found it."
        iconPath="sun.svg"
      />
    </div>

    <div class="spacer"></div>

    <p
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
    >When I’m not busy with any of the former, you’ll find me enjoying any of the following</p>
    <div
      class="interests"
      data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="2000"
      data-aos-delay="800"
    >
      <p>
        Skiing
        <br />Photography
        <br />Climbing
      </p>
      <p>
        Reading
        <br />Surfing
        <br />Chess
      </p>
      <p>
        Hiking
        <br />Learning
        <br />Foosball
      </p>
      <p>
        Cooking
        <br />Paintball
        <br />SCUBA
      </p>
    </div>

    <br />
    <br />
    <br />
    <br />
    <br />
  </div>
</template>

<script>
// @ is an alias to /src
import Card from "@/components/Card.vue";
import CareCard from "@/components/CareCard.vue";

// import Rellax from "../../node_modules/rellax/rellax.min.js";      // TODO ; get rellax working
// var rellax = new Rellax(".rellax");

export default {
  name: "home",
  components: {
    Card,
    CareCard
  },
  data() {
    return {
      designTitle: "I practice human-centered design",
      designText:
        "Why shouldn’t every website be grandma friendly? I get users from point A to Z without any friction. No ambiguities. No bloatware. No intrusion. Clean & simple.",
      designButton: "check out my work",
      devTitle: "I'm an agile developer",
      devText:
        "I make stuff... and break stuff! I’ve studied everything from Object-Oriented Design to Artificial Intelligence. I’m familiar with a handful of frameworks and I’m always looking for new ways of doing things.",
      devButton: "see what i'm building",
      web3Title: "I'm passionate about decentralization",
      web3Text:
        "We are witnessing the reinvention of value exchange, network protocol design, and so much more! Cryptocurrency and Web 3 has the power to disrupt every industry, and I can’t wait to see what the future holds for distributed computing.",
      web3Button: "view my crypto projects",
      musicTitle: "I live for music",
      musicText:
        "Whether it’s producing, djing, slappin' the bass, tinkering with hardware, audio engineering or even just listening... I can’t go one day without some kind of auditory stimulation.",
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
  // position: relative;
  display: flex;
  flex-direction: row;
  flex-basis: min-content;

  span {
    margin: auto;

    img {
      // TODO ; export white icons in figma w/ box shadow
      // box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.4);
    }
  }
}
#hi {
  text-shadow: 2px 4px 10px rgba(0, 0, 0, 0.06);
}
#me {
  text-shadow: 2px 4px 10px rgba(0, 0, 0, 0.12);
}
#ima {
  padding-top: $med;
  margin-bottom: $sm;
  display: inline-block;
  text-shadow: 2px 4px 10px rgba(0, 0, 0, 0.08);

  strong {
    font-weight: 600;
    color: white;
    @extend %quick-ease;

    &:hover {
      color: #04444d;
    }
  }
}

#scroll {
  padding-bottom: $med;
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
  width: $max-width - $lg;
  margin: auto;

  p {
    text-align: left;
    color: #d4d3d3;
  }
}
.home {
  padding-top: $sm * 3;
}
#scroll {
  width: $sm;
  display: inline-block;
}
</style>
