<template>
  <div>
    <articleTemplate />
  </div>
</template>
<script>
import articleTemplate from '~/components/article/articleTemplate'
export default {
  components: {
    articleTemplate
  },

  head() {
    return {
      title: 'Zenter Akupunkturklinikk Klepp | Akupunktur historie',
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
