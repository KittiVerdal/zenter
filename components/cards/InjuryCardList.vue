<template>
  <b-row>
    <CardItem
      v-for="card in injuryCards"
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
import CardItem from './CardItem'
import injuryCards from '../../constants/injuryCards'

export default {
  components: {
    CardItem
  },
  data: () => {
    return {
      injuryCards
    }
  }
}
</script>

<style lang="scss" scoped></style>
