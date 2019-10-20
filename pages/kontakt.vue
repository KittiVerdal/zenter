<template>
  <div>
    <parentHeader>
      <template v-slot:category>Kontaktdetaljer og åpningstider</template>
      <template v-slot:headline>
        Kontakt oss eller
        <br />
        <span class="[ header_headline--blue ]">kom innom i døra</span>?
      </template>
      <template v-slot:leadin>
        Nedenfor er en oversikt over noen av sykdommene og lidelsene hvor
        akupunktur kan være en aktuell behandlingsform, men det er mye mellom
        himmel og jord. Akupunktur bidrar til å få kroppen din i balanse. Dersom
        du er usikker på om akupunktur er den riktige behandligen for deg er du
        velkommen til en uforpliktende samtale hos oss.
      </template>
    </parentHeader>
    <contactRow></contactRow>
    <b-container fluid>
      <b-img class="imageLarge" fluid-grow src="../assets/images/kontakt.jpg"></b-img>
    </b-container>
  </div>
</template>

<script>
import parentHeader from '~/components/headers/parentHeader'
import contactRow from '~/components/elements/contactRow'
export default {
  components: {
    parentHeader,
    contactRow
  },
  head() {
    return {
      title: 'Klepp | Zenter Akupunkturklinikk | Kontakt oss',
      meta: [
        {
          name: 'description',
          content: 'Klinikken ligger midt i klepp sentrum på Jæren. Kort kjøreavstand fra både Stavanger og Sandnes. Gratis parkering rett utenfor'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  margin-top: -40px;
  &_headline--blue {
    color: $primaryLight;
  }
}
.container-fluid {
  padding-right: 0px;
  padding-left: 0px;
}
</style>
