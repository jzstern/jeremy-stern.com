<template>
  <div id="music">
    <!-- <h1>Music</h1> -->
    <!-- <p>One of my favorite things in life</p> -->
    <div class="content">
      <h2>Production</h2>
      <p>I've been teaching myself to produce with Ableton Live for the past ~5 years. Happy to license demos &/or create music of any/all genres for whatever you might need ^_^</p>
      <br>
      <br>
      <h2>Mixing/Mastering</h2>
      <p>
        I can provide mixing & mastering services for a variety of genres.
        <a
          href="mailto:jzstern@gmail.com"
        >Contact me</a> for rates.
      </p>
      <br>
      <br>
      <h2>Sound Design</h2>
      <p>I have some experience with doing sound design for cartoons, videos, and short films. Very interested in doing work for games (including music production)!</p>
      <br>
      <br>

      <h2>DJing</h2>
      <p>I've spun a mighty few events, both formal and informal, and would love to bring you on a sonic journey! I can cater to most genres and will happily record a mix for you.</p>

      <div class="soundcloud-links">
        <iframe
          scrolling="no"
          frameborder="no"
          allow="autoplay"
          src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/306399506&color=%23577561&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"
        ></iframe>
        <iframe
          scrolling="no"
          frameborder="no"
          allow="autoplay"
          src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/335712956&color=%23577561&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"
        ></iframe>
        <iframe
          scrolling="no"
          frameborder="no"
          allow="autoplay"
          src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/421592694&color=%23577561&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"
        ></iframe>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Music"
};
</script>

<style lang="scss" scoped>
@import "../styles/global.scss";

.soundcloud-links {
  margin-top: $sm;
  width: 100%;
  justify-content: center;
  text-align: center;
  display: inline-block;
}

.content {
  display: inline-block;
  text-align: left;
  width: $med * 5;
  // max-width: $med * 5;
}

iframe {
  width: $lg * 2;
  height: 480px;
  margin-bottom: $med;
}
</style>
