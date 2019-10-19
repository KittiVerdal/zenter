<template>
  <b-row>
    <CardItem
      v-for="card in treatmentCards"
      :key="card.id"
      :path="card.path"
      :alt="card.alt"
      :image-title="card.titleattr"
      :title="card.title"
      :sub-title="card.category"
    />      
  </b-row>
</template>

<script>
import CardItem from "./CardItem"
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

<style lang="scss" scoped>

</style>
