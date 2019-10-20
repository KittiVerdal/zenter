<template>
  <button class="[ btnOutlined ]">
    <slot />
  </button>
</template>
<script>
export default {}
</script>

<style lang="scss" scoped>
.btnOutlined {
  display: inline-block;
  padding: 1em;
  border: 2px solid $primary;
  border-radius: 3px;
  background-color: transparent;
  color: $primary;
  font-family: $zenterfont;
  border-radius: 50px;
  font-size: 1em;
  font-weight: 600;
  letter-spacing: 0.8px;
  line-height: 1;
  min-width: 200px;
  text-decoration: none;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.4s;

  &:hover {
    background: $primary;
    color: #fff;
    box-shadow: 0px 3px 30px 0px rgba($primary, 0.5);
    transition: 0.3s;
  }
}
</style>
