<template>
  <div>
    <parentHeader>

      <template v-slot:category>Pasientoversikt over ulike lidelser</template>
      <template v-slot:headline>
        Kan akupunktur
        <br />
        <span class="[ header_headline--blue ]">hjelpe meg</span>?
      </template>
      <template v-slot:leadin>
        Nedenfor er en oversikt over noen av sykdommene og lidelsene hvor
        akupunktur kan være en aktuell behandlingsform, men det er mye mellom
        himmel og jord. Akupunktur bidrar til å få kroppen din i balanse. Dersom
        du er usikker på om akupunktur er den riktige behandligen for deg er du
        velkommen til en uforpliktende samtale hos oss.
      </template>
    </parentHeader>

    <b-container class="[ cards--marginTop ]">
      <InjuryCardList />
    </b-container>
  </div>
</template>

<script>
import InjuryCardList from '~/components/cards/InjuryCardList'
import parentHeader from '~/components/headers/parentHeader'

export default {
  components: {
    InjuryCardList,
    parentHeader
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
