<template>
  <div class="wrapper">
    <TheNav />
    <TheSlideMenu />
    <div>
      <transition name="slide-fade" mode="out-in">
        <nuxt />
      </transition>
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

/*TRANSITIONS *************/
.fade-enter {
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.6s ease-out;
}

.fade-leave-to {
  opacity: 0;
}

.slide-fade-enter {
  opacity: 0;
  transform: translateY(10px);
}

.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 0.6s ease-in-out;
}

.slide-fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
