<template>
  <b-container fluid class="[ header header--background ]">
    <b-container>
      <b-row>
        <b-col sm="12">
          <h3 class="[ header_category ]">
            <slot name="category"></slot>
          </h3>
          <h1 class="[ header_headline ]">
            <slot name="headline"></slot>
          </h1>
          <p class="[ header_leadin ]">
            <slot name="leadin"></slot>
          </p>
        </b-col>
      </b-row>
    </b-container>
    <pulse />
  </b-container>
</template>

<script>
import pulse from '~/components/pulse/pulse'
export default {
  components: {
    pulse
  }
}
</script>

<style lang="scss" scoped>
.box {
  position: absolute;
  right: 20%;
  top: 10px;
  @media screen and (max-width: 1500px) {
    width: 200px;
    height: 200px;
  }
  @media screen and (max-width: 1140px) {
    width: 130px;
    height: 130px;
  }
  @media screen and (max-width: 800px) {
    width: 100px;
    height: 100px;
  }
  @media screen and (max-width: 769px) {
    display: none;
  }
}

.header {
  margin-top: -40px;
  font-family: $zenterfont;
  letter-spacing: 0.8px;
  &_category {
    padding-top: 150px;
    color: $primary;
    font-size: 16px;
    text-transform: uppercase;
    font-weight: 300;
  }
  &_headline {
    color: $white;
    font-size: 60px;
    font-weight: 600;
    @media screen and (max-width: 768px) {
      font-size: 45px;
    }
  }
  &_leadin {
    color: $white;
    @media screen and (max-width: 768px) {
      font-size: 16px;
    }
  }
  &--background {
    background-color: $secondary;
    font-size: 18px;
    font-weight: 300;
    letter-spacing: 1px;
    padding-bottom: 20px;
  }
}
</style>
