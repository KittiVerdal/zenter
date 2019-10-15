<template>
  <div>
    <TheNav />
    <div>
      <nuxt />
    </div>
    <TheFooter />
  </div>
</template>

<script>
import TheNav from './partials/TheNav'
import TheFooter from './partials/TheFooter'
export default {
  components: {
    TheNav,
    TheFooter
    
  }
}
</script>
