<template>
  <b-row>
    <CardItem
      v-for="card in treatmentCards"
      :key="card.id"
      :id="card.id"
      :path="card.path"
      :alt="card.alt"
      :image-title="card.titleattr"
      :title="card.title"
      :sub-title="card.category"
      type="behandling"
    />
  </b-row>
</template>

<script>
import CardItem from './CardItem'
import treatmentCards from '../../constants/treatmentCards'

export default {
  components: {
    CardItem
  },
  data: () => {
    return {
      treatmentCards
    }
  }
}
</script>

<style lang="scss" scoped></style>
