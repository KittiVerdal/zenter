<template>
  <b-col xl="3" lg="4" md="6" class="[ card_image ]">
    <nuxt-link :to="{ path: type + '/' + id }">
      <b-card
        class="[ card_container ]"
        overlay
        :img-src="path"
        :img-alt="title"
        :img-title="title"
        :title="title"
        :sub-title="title"
      />
    </nuxt-link>
  </b-col>
</template>

<script>
export default {
  name: 'CardItem',
  props: {
    path: String,
    title: String,
    type: String,
    id: Number
  }
}
</script>

<style lang="scss" scoped>
h6.text-muted {
  color: $primary !important;
  text-transform: uppercase;
  font-size: 14px;
  @media screen and (max-width: 768px) {
    font-size: 24px;
  }
  @media screen and (max-width: 550px) {
    font-size: 20px;
  }
}
h4 {
  padding-top: 85%;
  font-weight: 900;
  font-size: 27px;
  @media screen and (max-width: 768px) {
    font-size: 54px;
  }
  @media screen and (max-width: 550px) {
    font-size: 35px;
  }
}
a {
  cursor: pointer;
  color: $white;
}
.card {
  &_title {
    z-index: 100;
  }
  &_container {
    margin-bottom: 25px;
    font-family: $zenterfont;
    font-weight: 900;
    border: 0;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    &:hover {
      box-shadow: 0 14px 28px rgba(0, 0, 0, 0.35),
        0 10px 10px rgba(0, 0, 0, 0.37);
    }
  }
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
