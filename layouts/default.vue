<template>
  <div>
    <TheNav />
    <TheSlideIn />
    <div>
      <nuxt />
    </div>
    <TheFooter/>
  </div>
</template>

<script>
import TheNav from './partials/TheNav'
import TheSlideIn from './partials/TheSlidein' 
import TheFooter from './partials/TheFooter'

export default {
  components: {
    TheNav,
    TheSlideIn,
    TheFooter
  }
  
}
</script>

<style scoped>

</style>

