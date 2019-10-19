<template>
  <div>
    <videoHeader />
    <div class="container">
      <h1>INDEXpage</h1>
      <b-container>
        <b-row>
          <b-col md="6">
            <videoCard />
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>
<script>
import videoHeader from '~/components/videos/videoHeader'
import videoCard from '~/components/cards/videoCard'

export default {
  components: {
    videoHeader,
    videoCard
  },

  head() {
    return {
      title: 'Zenter Akupunkturklinikk Klepp | Alternativ behandling',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'Behandling gjennom akupunktur er godt dokumentert for en rekke lidelser og plager. Gi kroppen de rette verktøyene for å øke kvaliteten i din hverdag.'
        }
      ]
    }
  }
}
</script>
