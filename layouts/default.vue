<template>
  <div class="wrapper">
    <TheNav />
    <TheBurger />
    <TheSlideMenu />
    <transition name="fade">
      <TheSidebar>
        <ul class="sidebar-panel-nav">
          <li>
            <nuxt-link to="/">Hjem</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/plager">Plager</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/behandlinger">Behandlinger</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/priser">Priser</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/kontakt">Kontakt</nuxt-link>
          </li>
        </ul>
      </TheSidebar>
    </transition>
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
//import TheSlideMenu from './partials/TheSlideMenu'
import TheFooter from './partials/TheFooter'
import TheBurger from '../components/menu/burger'
import TheSidebar from '../components/menu/sidebar'
export default {
  components: {
    TheNav,
    //    TheSlideMenu,
    TheFooter,
    TheBurger,
    TheSidebar
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

.main-nav {
  display: flex;
  justify-content: space-between;
  padding: 0.5rem 0.8rem;
}

ul.sidebar-panel-nav {
  list-style-type: none;
}

ul.sidebar-panel-nav > li > a {
  color: #fff;
  text-decoration: none;
  font-size: 22px;
  display: block;
  padding: 20px;
  margin-left: -40px;
  font-family: $zenterfont;
  letter-spacing: 1px;
  font-weight: 300;
  &:hover {
    background-color: rgba($black, 0.3);
    border-radius: 5px;
    color: $primary;
  }
  &:active {
    background-color: rgba($black, 0.3);
    border-radius: 5px;
    color: $primary;
  }
  &:focus {
    background-color: rgba($black, 0.3);
    border-radius: 5px;
    color: $primary;
  }
}
</style>
