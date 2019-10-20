<template>
  <div id="app" class="[ video ]">
    <video
      autoplay
      loop
      muted
      ref="videoRef"
      src="~assets/images/Frontmovie-styles_2.mp4"
      id="video-container"
      width="100%"
      alt="Bilde av ung, sunn dame på fjellet"
    ></video>
    <div class="[ header header_container ]">
      <h2 class="[ header header_subHeader ]">Akupunktur</h2>
      <h1 class="[ header header_headline ]">
        Kvalitet i hver
        <br />time hver dag
      </h1>
      <p class="[ header header_text ]">
        Effekten av akupunktur er godt dokumentert for en rekke lidelser. Gi
        kroppen de riktige verktøyene for å øke kvaliteten i din hverdag.
      </p>
      <primaryBtnOutline :handleClick="navigate">Se våre behandlinger</primaryBtnOutline>
    </div>
    <pulse />
  </div>
</template>
<script>
import primaryBtnOutline from '~/components/buttons/primaryBtnOutline'
import pulse from '~/components/pulse/pulse'

export default {
  components: {
    primaryBtnOutline,
    pulse
  },
  methods: {
    navigate: function() {
        this.$router.push({
            path: '/behandlinger'
        })
    }
  }
}
</script>

<style lang="scss" scoped>
.box {
  position: absolute;
  right: 30%;
  top: 10px;
  @media screen and (max-width: 1500px) {
    width: 200px;
    height: 200px;
  }
  @media screen and (max-width: 1140px) {
    width: 130px;
    height: 130px;
  }
  @media screen and (max-width: 800px) {
    width: 100px;
    height: 100px;
  }
  @media screen and (max-width: 769px) {
    display: none;
  }
}

.video {
  margin-top: -80px;
  z-index: 1;
  @media screen and (max-width: 769px) {
    margin-top: 0px;
  }
}

.header {
  font-family: $zenterfont;
  letter-spacing: 0.8px;
  color: $white;

  &_container {
    background-color: rgba($secondaryDark, 0.85);
    width: 40%;
    position: absolute;
    top: 200px;
    right: 50px;
    padding: 40px;
    border-radius: 10px;
    @media screen and (max-width: 1250px) {
      top: 150px;
    }
    @media screen and (max-width: 1050px) {
      top: 120px;
    }
    @media screen and (max-width: 900px) {
      width: 50%;
      right: 30px;
      top: 100px;
      padding: 20px;
    }
    @media screen and (max-width: 769px) {
      position: relative;
      width: 100%;
      right: 0;
      top: -10px;
      border-radius: 0px;
      background-color: rgba($secondaryDark, 1);
    }
  }
  &_subHeader {
    font-weight: 400;
    text-transform: uppercase;
    font-size: 1.5em;
    color: $primary;
    @media screen and (max-width: 1250px) {
      font-size: 1.2em;
    }
  }
  &_headline {
    font-weight: 700;
    font-size: 4.8em;
    line-height: 80px;
    @media screen and (max-width: 1440px) {
      font-size: 4em;
      line-height: 70px;
    }
    @media screen and (max-width: 1250px) {
      font-size: 3em;
      line-height: 50px;
    }
    @media screen and (max-width: 980px) {
      font-size: 2.3em;
      line-height: 40px;
    }
    @media screen and (max-width: 900px) {
      font-size: 4em;
      line-height: 65px;
    }
  }
  &_text {
    font-size: 1.2em;
    padding: 20px 0px;
    @media screen and (max-width: 1250px) {
      font-size: 1em;
      padding: 10px 0px;
    }
    @media screen and (max-width: 980px) {
      font-size: 18px;
      padding: 5px 0px;
    }
  }
}
.btnOutlined {
  margin-right: 20px;
  @media screen and (max-width: 1440px) {
    min-width: 170px;
  }
  @media screen and (max-width: 800px) {
    min-width: 100%;
  }
}
</style>
