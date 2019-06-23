<template>
  <div class="home">
    <p id="hi">Hi, my name is</p>
    <h1>Jeremy Stern</h1>

    <p id="ima">
      I'm a
      <strong>Product Designer</strong>,
      <strong>Developer</strong>, and
      <strong>Sound Wizard</strong>
    </p>

    <Card
      type="design"
      :title="this.designTitle"
      :text="this.designText"
      :button="this.designButton"
    />

    <Card type="development" :title="this.devTitle" :text="this.devText" :button="this.devButton"/>

    <Card type="web3" :title="this.web3Title" :text="this.web3Text" :button="this.web3Button"/>

    <Card type="music" :title="this.musicTitle" :text="this.musicText" :button="this.musicButton"/>
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
  data: function() {
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
      musicButton: "listen to my sounds"
    };
  }
};
</script>

<style lang="scss" scoped>
#hi {
  padding-top: 180px;
}
#ima {
  padding: 120px 0;
}
h1 {
  // font-weight: 600;
}
strong {
  font-weight: 600;
}
</style>
