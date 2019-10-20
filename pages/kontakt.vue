<template>
  <div>
    <parentHeader>
      <template v-slot:category
        >Kontaktdetaljer og åpningstider</template
      >
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
  </div>
</template>

<script>
import parentHeader from '~/components/headers/parentHeader'
export default {
  components: {
    parentHeader
  },
  head() {
    return {
      title: 'Klepp | Zenter Akupunkturklinikk | Kontakt oss',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'Klinikken ligger midt i klepp sentrum på Jæren. Kort kjøreavstand fra både Stavanger og Sandnes. Gratis parkering rett utenfor'
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
