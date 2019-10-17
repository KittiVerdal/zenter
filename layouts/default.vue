<template>
  <div class="wrapper">
    <TheNav />
    <TheSlideMenu />
    <div>
      <nuxt />
    </div>
    <TheFooter />
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
.wrapper {
  min-height: 100vh;
  display: grid;
  grid-template-rows: auto 1fr auto;
}

a {
  color: $primary;
  &:hover {
    color: $tertiaryMedium;
    text-decoration: none;
  }
}
</style>