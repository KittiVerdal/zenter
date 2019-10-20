<template>
  <div>
    <parentHeader>
      <template v-slot:category
        >Pasientoversikt over ulike behandlinger</template
      >
      <template v-slot:headline>
        <span class="[ header_headline--blue ]">Behandlingsmeny</span>
        <br />og priser
      </template>
      <template v-slot:leadin>
        Nedenfor er en oversikt over behandling vi tilbyr her hos Zenter
        Akupunkturklinikk. Behandlingne foregår hovedsaklig i våre lokaler på
        Klepp. Akupunktur bidrar til å få kroppen din i balanse. Dersom du er
        usikker på om akupunktur er den riktige behandligen for deg er du
        velkommen til en uforpliktende samtale hos oss.
      </template>
    </parentHeader>

    <b-container class="[ cards--marginTop ]">
      <TreatmentCardList />
    </b-container>
  </div>
</template>

<script>
import TreatmentCardList from '~/components/cards/TreatmentCardList'
import parentHeader from '~/components/headers/parentHeader'

export default {
  components: {
    parentHeader,
    TreatmentCardList
  },
  head() {
    return {
      title: 'Zenter Akupunkturklinikk Klepp | Behandlingsmeny',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'Dyktig autorisert akupunktør. Kort ventetid. Muskelsmerter, leddplager, hodepine, barnløshet, utbrenthet, allergi, slitasje m.m. Gratis parkering.'
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
.cards {
  &--marginTop {
    margin-top: 40px;
  }
}
</style>
