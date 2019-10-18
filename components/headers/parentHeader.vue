<template>
  <b-container fluid class="[ header--background ]">
    <b-container>
      <b-row>
        <b-col sm="12">
          <h3 class="[ header_category ]">
            <slot name="category"></slot>
          </h3>
          <h1 class="[ header_headline ]">
            <slot name="headline"></slot>
          </h1>
          <p>
            <slot name="leadin"></slot>
          </p>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
</style>
    