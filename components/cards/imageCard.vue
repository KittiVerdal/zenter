<template>
  <div>
    <a href="/">
      <div
        class="image"
        v-for="articleCard in articleCards"
        :key="articleCard.id"
        @mouseover="hovered = true"
        @mouseleave="hovered = null"
      >
        <transition name="fade">
          <div class="overlay" v-if="hovered === articleCard.id"></div>
        </transition>
        <img
          :src="articleCard.path"
          :alt="articleCard.alt"
          :title="articleCard.titleattr"
        />
        <h3>{{ articleCard.category }}</h3>
        <h2>{{ articleCard.title }}</h2>
      </div>
    </a>
  </div>
</template>

<script>
import { articleCards } from '../../constants/articleCards'

export default {
  data: function() {
    return {
      articleCards
    }
  }
}
</script>

<style lang="scss" scoped>
a {
  cursor: pointer;
}
.image {
  height: auto;
  width: 300px;
}
.overlay {
  background: rgba($secondaryDark, 0.7);
  height: 300px;
  width: auto;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
