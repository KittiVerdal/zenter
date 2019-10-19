<template>
  <div class="sidebar">
    <div
      class="sidebar-backdrop"
      @click="closeSidebarPanel"
      v-if="isPanelOpen"
    ></div>
    <transition name="slide">
      <div v-if="isPanelOpen" class="sidebar-panel">
        <slot></slot>
        <pulse />
      </div>
    </transition>
  </div>
</template>
<script>
import pulse from '~/components/pulse/pulse'
export default {
  components: {
    pulse
  },
  data: () => ({
    isPanelOpen: true
  }),
  methods: {
    closeSidebarPanel() {
      this.isPanelOpen = false
    }
  }
}
</script>
<style></style>

<style lang="scss" scoped>
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.2s ease;
}

.slide-enter,
.slide-leave-to {
  transform: translateX(-100%);
  transition: all 150ms ease-in 0s;
}

.sidebar-backdrop {
  background-color: rgba(0, 0, 0, 0.8);
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 888;
  cursor: pointer;
}

.sidebar-panel {
  overflow-y: auto;
  background-image: url('../../assets/images/mobil-panel.svg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: bottom right;
  position: fixed;
  left: 0;
  top: 0;
  height: 100vh;
  z-index: 999;
  padding: 3rem 20px 2rem 20px;
  width: 320px;
}
.box {
  position: absolute;
  right: -150px;
  bottom: -170px;
  @media screen and (max-width: 1500px) {
    width: 200px;
    height: 200px;
  }
}
</style>
