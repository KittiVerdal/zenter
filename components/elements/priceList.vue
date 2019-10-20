<template>
  <b-container>
    <b-col>
      <priceListItem>
        <template v-slot:treatment
          >Akupunktur - Førstegangskonsultasjon</template
        >
        <template v-slot:amount
          >680</template
        >
        <template v-slot:description
          >Akupunktur inkludert førstegangskonsultasjon, varighet fra ca 1 time
          til 1,5 time</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Akupunktur - Oppfølgingstime</template
        >
        <template v-slot:amount
          >480</template
        >
        <template v-slot:description
          >Akupunktur, oppfølgingstime, varighet ca 30 minutter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Kopping</template
        >
        <template v-slot:amount
          >350</template
        >
        <template v-slot:description
          >Varighet 30 minutter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Kosmetisk Akupunktur</template
        >
        <template v-slot:amount
          >699</template
        >
        <template v-slot:description
          >Første konsultasjon</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Kosmetisk Akupunktur</template
        >
        <template v-slot:amount
          >699</template
        >
        <template v-slot:description
          >Oppfølgingstime</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Elektroakupunktur</template
        >
        <template v-slot:amount
          >480</template
        >
        <template v-slot:description
          >Bruk av strøm på akupunkturpunkter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Guasha</template
        >
        <template v-slot:amount
          >480</template
        >
        <template v-slot:description>
          Guasha (på kinesisk 刮痧) er en behandlingsmetode en flat plate og
          skraper den langs huden til pasienten. Brukes for stive, smertefulle
          og betente muskler i likt med massasje.
        </template>
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Kombi: Akupunktur + Kopping</template
        >
        <template v-slot:amount
          >550</template
        >
        <template v-slot:description
          >Varighet 30-45 minutter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Kombi: Akupunktur + Triggerpunkt</template
        >
        <template v-slot:amount
          >580</template
        >
        <template v-slot:description
          >Varighet 30-45 minutter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Kombi: Akupunktur + Triggerpunkt + Kopping</template
        >
        <template v-slot:amount
          >680</template
        >
        <template v-slot:description
          >Varighet 60 minutter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Moxa Varmebehandling</template
        >
        <template v-slot:amount
          >50</template
        >
        <template v-slot:description
          >Varmebehandling med brenning av urter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Ørelysbehandling</template
        >
        <template v-slot:amount
          >450</template
        >
        <template v-slot:description
          >Varighet 20 minutter</template
        >
      </priceListItem>
      <priceListItem>
        <template v-slot:treatment
          >Øreakupunktur tillegg</template
        >
        <template v-slot:amount
          >120</template
        >
        <template v-slot:description
          >Tillegg etter avtale</template
        >
      </priceListItem>
      <p class="[ picelist_text ]">
        *Avbestilling kun pr. telefon. Manglende oppmøte eller avbestilling
        senere en 48 timer før avtalt tid blir fakturert og belastet 100%.
      </p>
    </b-col>
  </b-container>
</template>

<script>
import priceListItem from '~/components/elements/priceListItem'
export default {
  components: {
    priceListItem
  }
}
</script>

<style lang="scss" scoped>
.picelist_text {
  font-family: $zenterfont;
  font-style: italic;
  font-size: 12px;
  margin-bottom: 50px;
  margin-top: 15px;
}
</style>
