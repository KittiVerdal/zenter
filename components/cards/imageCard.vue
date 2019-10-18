<template>
  <b-row>
    <div class="image" v-for="articleCard in articleCards" :key="articleCard.id">
      <b-col md="3">
        <img :src="articleCard.path" :alt="articleCard.alt" :title="articleCard.titleattr" />
        <h3>{{ articleCard.category }}</h3>
        <h2>{{ articleCard.title }}</h2>
      </b-col>
    </div>
  </b-row>
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
