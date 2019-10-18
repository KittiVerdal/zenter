<template>
  <div>
    <videoHeader />
    <div class="container">
      <h1>INDEXpage</h1>
    </div>
  </div>
</template>
<script>
import videoHeader from '~/components/videos/videoHeader'

export default {
  components: {
    videoHeader
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
