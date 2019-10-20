<template>
  <b-container>
    <b-col>
      <priceListItem />
      <p>
        *Avbestilling kun pr. telefon. Manglende oppmøte eller avbestilling
        senere en 48 timer før avtalt tid blir fakturert og belastet 100%.
      </p>
    </b-col>
  </b-container>
</template>

<script>
import priceListItem from '~/components/elements/priceListItem'
export default {
  components: {
    priceListItem
  }
}
</script>
