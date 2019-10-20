<template>
  <b-card class="[ price price_list ]">
    <h4 class="[ price price_title ]">
      Treatment
      <span class="[ price_title--priceAmount ]">695</span>
      <span class="[ price_title--currency ]">Nok</span>
    </h4>
    <b-card-text class="[ price price_description ]"
      >With supporting text below as a natural lead-in to additional
      content.</b-card-text
    >
    <smallButton>Book time</smallButton>
  </b-card>
</template>

<script>
import smallButton from '~/components/buttons/smallButton'

export default {
  components: {
    smallButton
  }
}
</script>

<style lang="scss" scoped>
.price {
  font-family: $zenterfont;
  &_list {
    margin-top: 20px;
    margin-left: -15px;
    margin-right: -15px;
  }
  &_title {
    font-weight: 400px;
    font-size: 28px;
    &--priceAmount {
      float: right;
      font-size: 24px;
      color: $greyDark;
      font-weight: 300;
    }
    &--currency {
      float: right;
      font-size: 18px;
      color: $greyDark;
      font-weight: 300;
    }
  }
  &_description {
    color: $greyDark;
  }
}
</style>
