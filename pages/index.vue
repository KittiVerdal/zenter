<template>
  <div>
    <videoHeader />
    <div class="container">
      <h1>INDEXpage</h1>
      <b-container>
        <b-row>
          <b-col md="6"></b-col>
        </b-row>
      </b-container>
    </div>
    <bookingForm />
  </div>
</template>
<script>
import videoHeader from '~/components/videos/videoHeader'
import videoCard from '~/components/cards/videoCard'
import bookingForm from '~/components/forms/bookingform'

export default {
  components: {
    videoHeader,
    videoCard,
    bookingForm
  },

  head() {
    return {
      title: 'Zenter Akupunkturklinikk Klepp | Alternativ behandling',
      meta: [
        {
          name: 'description',
          content: 'Behandling gjennom akupunktur er godt dokumentert for en rekke lidelser og plager. Gi kroppen de rette verktøyene for å øke kvaliteten i din hverdag.'
        }
      ]
    }
  }
}
</script>
