<template>
  <div class="design">
    <div class="content">
      <h2 id="portfolio">
        <a href="https://dribbble.com/jzstern" target="_blank">Portfolio</a>
      </h2>
      <!-- <i>I primarily use Figma, but have experience with Sketch</i> -->
      <!-- <p>Below are a handful of projects I've worked on for hackathons, design challenges, and just for fun. Hit me up if you'd like to learn a bit more about my process!</p> -->

      <carousel :data="slides"></carousel>
      <div id="images">
        <design-preview
          v-for="item in previews"
          :key="item.title"
          :title="item.title"
          :text="item.text"
          :url="item.url"
          :previewUrl="item.previewUrl"
        ></design-preview>

        <!-- <a href="https://imgur.com/gallery/IuOT5D1" target="_blank">
        <img src="https://i.imgur.com/8Xy54Qa.png">
      </a>
      <a href="https://imgur.com/gallery/lltFBLZ" target="_blank">
        <img src="https://i.imgur.com/Gq6Up5G.png">
        </a>-->
      </div>
      <h2>Philosophy</h2>
      <i>“People ignore design that ignores people.” - Frank Chimero</i>
      <!-- <p>- Frank Chimero</p> -->
      <p>Design is one of the most important yet overlooked foundations of digital products. No matter how much high level utility a service provides, user experience will make or break a product.</p>
      <p>Together, we can bring ideas to their full potential. Everything starts with defining the problem. It's not just the how, but also the why.</p>
      <p>Less is more.</p>
    </div>
  </div>
</template>

<script>
import DesignPreview from "../components/DesignPreview.vue";
import VueCarousel from "@chenfengyuan/vue-carousel";
export default {
  name: "Design",
  components: {
    DesignPreview,
    VueCarousel
  },
  data() {
    return {
      previews: [
        {
          title: "Lightning Network App Store",
          text:
            "I was given a loose list of requirements to make a directory for applications that use the Bitcoin Lightning Network.",
          url: "https://imgur.com/gallery/IuOT5D1",
          previewUrl:
            "https://cdn.dribbble.com/users/3030370/screenshots/6626797/home.png"
          // previewUrl: "https://i.imgur.com/8Xy54Qa.png"
        },
        {
          title: "Rocky Road",
          text:
            "Concept I made for a ski/snowboard ride share app that would connect drivers with extra space in their car to people that need a cheap lift up.",
          url: "https://imgur.com/gallery/lltFBLZ",
          previewUrl: "https://i.imgur.com/Gq6Up5G.png"
        },
        {
          title: "Flight Fund",
          text:
            "I snuck into ETH Denver for a day and worked with my friend's hackathon group to create their project's interface. Worked through.. ",
          url: "https://imgur.com/a/eVDXUfz",
          previewUrl: "https://i.imgur.com/5ERx61S.jpg"
        }
        // {
        //   title: "Cryptocurrency Converter",
        //   text:
        //     "Result of a Daily UI Challenge prompt. Minimalist approach to converting the value of FIAT currency to various popular cryptocurrencies.",
        //   url: "https://dribbble.com/shots/5868967-Crypto-Converter",
        //   previewUrl:
        //     "https://cdn.dribbble.com/users/3030370/screenshots/5868967/day_4__calculator_-_view_2_.png"
        // }
        // {
        //   title: "Credit Card Checkout",
        //   text:
        //     "Another Daily UI Challenge prompt for a generic credit card checkout for a shopping app.",
        //   url: "https://i.imgur.com/nsSSSmu.png",
        //   previewUrl: "https://i.imgur.com/nsSSSmu.png"
        // },
        // {
        //   title: "Setting Page",
        //   text: "Concept for a generic settings page on a mobile app.",
        //   url: "https://dribbble.com/shots/5904993-Settings-Page/attachments",
        //   previewUrl:
        //     "https://cdn.dribbble.com/users/3030370/screenshots/5904993/settings.png"
        // }
      ],
      slides: [
        '<div class="example-slide">Slide 1</div>',
        '<div class="example-slide">Slide 2</div>',
        '<div class="example-slide">Slide 3</div>'
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

.example-slide {
  align-items: center;
  background-color: #666;
  color: #999;
  display: flex;
  font-size: 1.5rem;
  justify-content: center;
  min-height: 10rem;
}
</style>
