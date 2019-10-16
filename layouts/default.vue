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

<style scoped>

</style>

