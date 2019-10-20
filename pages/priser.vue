<template>
  <div>
    <parentHeader>
      <template v-slot:category>Om akupunktur</template>
      <template v-slot:headline>
        <span class="[ header_headline--blue ]">Hva er akupunktur</span>,
        <br />og hvorfor virker det?
      </template>
      <template v-slot:leadin>
        Nedenfor er en oversikt over noen av sykdommene og lidelsene hvor
        akupunktur kan være en aktuell behandlingsform, men det er mye mellom
        himmel og jord. Akupunktur bidrar til å få kroppen din i balanse. Dersom
        du er usikker på om akupunktur er den riktige behandligen for deg er du
        velkommen til en uforpliktende samtale hos oss.
      </template>
    </parentHeader>
    <pageTopicHeader />
  </div>
</template>

<script>
import parentHeader from '~/components/headers/parentHeader'
import pageTopicHeader from '~/components/headers/pageTopicHeader'
export default {
  components: {
    parentHeader,
    pageTopicHeader
  },
  head() {
    return {
      title: 'Zenter Akupunkturklinikk | Akupunktur mot smerte og sykdom',
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
<style lang="scss" scoped>
.header_headline--blue {
  color: $primaryLight;
}
</style>
