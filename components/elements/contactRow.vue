<template>
  <div>
    <b-container>
      <b-row>
        <b-col md="4">
          <b-img
            src="~/assets/images/ring.svg"
            class="[ contact_icon ]"
            alt="Zenter Akupunkturklinikk ring oss icon med snakkeboble"
            title="Zenter Akupunkturklinikk ring oss icon med snakkeboble"
          ></b-img>
          <h3 class="[ contact_title ]">Kontakt oss</h3>
          <h4 class="[ contact_title--sub ]">Telefon 905 56 932</h4>
          <p class="[ contact_title--bodyText ]">Send e-post til post@zenter.no</p>
        </b-col>
        <b-col md="4">
          <b-img
            src="~/assets/images/apent.svg"
            class="[ contact_icon ]"
            alt="Zenter Akupunkturklinikk ring oss icon med snakkeboble"
            title="Zenter Akupunkturklinikk ring oss icon med snakkeboble"
          ></b-img>
          <h3 class="[ contact_title ]">Åpningstider</h3>
          <h4 class="[ contact_title--sub ]">07:00 - 19:00</h4>
          <p class="[ contact_title--bodyText ]">Mandag, tirsdag og fredag</p>
        </b-col>
        <b-col md="4">
          <b-img
            src="~/assets/images/besok.svg"
            class="[ contact_icon ]"
            alt="Zenter Akupunkturklinikk ring oss icon med snakkeboble"
            title="Zenter Akupunkturklinikk ring oss icon med snakkeboble"
          ></b-img>
          <h3 class="[ contact_title ]">Besøk oss</h3>
          <h4 class="[ contact_title--sub ]">Kjøpmannsbrotet 5</h4>
          <p class="[ contact_title--bodyText ]">4352 Kleppe</p>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<style lang="scss" scoped>
.contact {
  &_icon {
    width: 70%;
    display: block;
    margin: 0 auto;
    margin-top: 20px;
  }
  &_title {
    font-family: $zenterfont;
    text-align: center;
    margin-top: 10px;
    font-weight: 600;
    &--sub {
      text-align: center;
    }
    &--bodyText {
      font-family: $zenterfont;
      text-align: center;
      font-size: 18px;
      margin-bottom: 30px;
    }
  }
}

.container-fluid {
  padding-right: 0px;
  padding-left: 0px;
}
</style>
    