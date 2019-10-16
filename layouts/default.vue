<template>
  <div>
    <TheNav />
    <TheSlideMenu />
    <div>
      <nuxt />
    </div>
    <TheFooter/>
  </div>
</template>

<script>
import TheNav from './partials/TheNav'
import TheSlideMenu from './partials/TheSlideMenu' 
import TheFooter from './partials/TheFooter'

export default {
  components: {
    TheNav,
    TheSlideMenu,
    TheFooter
  }
  
}
</script>

<style lang="scss">
a{
  color:$primary;
  &:hover{
    color:$tertiaryMedium;
    text-decoration:none;
  }
}
</style>

