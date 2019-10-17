<template>
  <div id="app" class="[ video ]">
    <video ref="videoRef" src="~assets/images/Frontmovie-styles_2.mp4" id="video-container" width="100%" alt="Bilde av ung, sunn dame på fjellet" controls></video>
    <b-img src="~/assets/images/circle270x270.svg" class="[ cicles ]" alt="Animerte sirkler"></b-img>
    <div class="[ header header_container ]">
      <h2 class="[ header header_subHeader ]">Akupunktur</h2>
      <h1 class="[ header header_headline ]">Kvalitet i hver<br />time hver dag</h1>
      <p class="[ header header_text ]">Effekten av akupunktur er godt dokumentert for en rekke lidelser. Gi kroppen de riktige verktøyene for å øke kvaliteten i din hverdag.</p>
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

.header{
    font-family: $zenterfont;
    letter-spacing: 0.8px;
    color:$white;

   &_container{
       background-color: rgba($secondaryDark, .7);
       width: 40%;
       position:absolute;
       top:200px;
       right:50px;
       padding:40px;
   }
   &_subHeader{
       font-weight: 400;
       text-transform: uppercase;
       font-size: 1.5em;
       color: $primary;
   }
   &_headline{
       font-weight: 700;
       font-size:4.8em;
       line-height: 80px;
   }
   &_text{
       font-size: 1.2em;
       padding:20px 0px; 
   }
}
.btnOutlined {
    margin-right:20px;
}
</style>
