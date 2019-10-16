<template>
  <div>
    <TheNav />
    <TheSlidein />
    <!-- <main id="page-wrap"></main> -->
    <div>
      <nuxt />
    </div>
    <TheFooter/>
  </div>
</template>

<script>
import TheNav from './partials/TheNav'
import TheSlidein from './partials/TheSlidein'
import TheFooter from './partials/TheFooter'

export default {
  components: {
    TheNav,
    TheSlidein,
    TheFooter
  }
  
}
</script>
