<template>
  <div class="container">
    <h1>Plager</h1>
    <b-container>
      <b-row>
        <imageCard />
      </b-row>
    </b-container>
  </div>
</template>
<script>
import imageCard from '~/components/cards/imageCard'

export default {
  components: {
    imageCard
  },

  head() {
    return {
      title: 'title on Plager page comes here',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'page description is written in more detail here for SEO'
        }
      ]
    }
  }
}
</script>
