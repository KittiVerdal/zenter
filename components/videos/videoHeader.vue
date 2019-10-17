<template>
  <div id="app" class="[ video ]">
    <video ref="videoRef" src="~assets/images/Frontmovie-styles_2.mp4" id="video-container" width="100%" controls></video>
    <b-img src="~/assets/images/circle270x270.svg" class="[ footer_logo  footer_logo--small ]" alt="Logo Akupunkturforeningen" title="Logo Akupunkturforeningen"></b-img>
    <div class="[ header_container ]">
      <h2 class="[ header_subHeader ]">Akupunktur</h2>
      <h1 class="[ header_headline ]">Kvalitet i hver<br />time hver dag</h1>
      <p class="[ header_text ]">Effekten av akupunktur er godt dokumentert for en rekke lidelser. Gi kroppen de rette verktøyene for å øke kvaliteten i din hverdag.</p>
      <primaryBtnOutline>Book online</primaryBtnOutline>
      <primaryBtnOutline>Ring oss</primaryBtnOutline>
    </div>
  </div>
</template>


<script>
import primaryBtnOutline from '~/components/buttons/primaryBtnOutline'

export default {
    components:{
        primaryBtnOutline
    },

      mounted: function() {
    this.$refs.videoRef.play();
  }
}
</script>

<style lang="scss" scoped>
.video {
    margin-top:-80px;
    z-index: 1;
    }
</style>
