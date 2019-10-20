<template>
  <div>
    <parentHeader>
      <template v-slot:category
        >Behandlingsmeny</template
      >
      <template v-slot:headline>
        <span class="[ header_headline--blue ]">Timebestilling</span>
        <br />og priser
      </template>
      <template v-slot:leadin>
        Ring og bestill på telefon 905 56 932 eller book time online nedenfor.
        <br />Vi har telefontid alle hverdager mellom 08:00 og 16:00. Online
        bookinger blir besvart fortløpende.
      </template>
    </parentHeader>
    <priceList />
    <pageTopicHeader />
    <bookingform />
  </div>
</template>

<script>
import parentHeader from '~/components/headers/parentHeader'
import pageTopicHeader from '~/components/headers/pageTopicHeader'
import priceList from '~/components/elements/priceList'
import bookingform from '~/components/forms/bookingform'
export default {
  components: {
    parentHeader,
    pageTopicHeader,
    priceList,
    bookingform
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
