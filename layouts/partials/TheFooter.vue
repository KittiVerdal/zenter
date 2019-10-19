<template>
  <b-container fluid class="[ footer_container ]">
    <b-container>
      <b-row>
        <b-col lg="2">
          <b-img
            src="~/assets/images/zenter.svg"
            class="[ footer_logo ]"
            alt="Zenter Akupunkturklinikk logo"
            title="Zenter Akupunkturklinikk logo"
          ></b-img>
        </b-col>
        <b-col lg="4" class="[ footer_colunm ]">
          <h4 class="[ footer_header ]">Åpningstider</h4>
          <p class="[ footer_text ]">
            Mandag:
            <span class="[ footer_text--right ]">07:00 - 19:00</span>
            <br />Tirsdag:
            <span class="[ footer_text--extra ]">07:00 - 19:00</span>
            <br />Torsdag:
            <span class="[ footer_text--right ]">07:00 - 19:00</span>
          </p>
          <p class="[ footer_text ]">Onsdag og fredag åpent etter avtale</p>
          <p class="[ footer_text ]">
            Telefontid alle hverdager fra 08:00-16:00
            <br />Avbestilling av timer kun pr telefon.
          </p>
        </b-col>

        <b-col lg="3">
          <h4 class="[ footer_header ]">Telefon: 905 56 932</h4>
          <h4 class="[ footer_header footer_header--marginTop ]">Adresse</h4>
          <p class="[ footer_text ]">
            Kjøpmannsbrotet 5,
            <br />4351 Kleppe
          </p>
          <h4 class="[ footer_header footer_header--marginTop ]">
            Finn frem til oss
          </h4>
          <p class="[ footer_text ]">
            <b-link
              href="https://www.google.com/maps/place/Zenter+akupunkturklinikk/@58.7800823,5.6205791,17z/data=!3m1!4b1!4m5!3m4!1s0x463a47c1eebc60c9:0x857b7c9d01f7c56!8m2!3d58.7800795!4d5.6227624"
              >Åpne adresse i Google maps her»</b-link
            >
          </p>
        </b-col>

        <b-col lg="3" alin>
          <primaryBtnOutline>Admin log in</primaryBtnOutline>
          <p class="[ footer_text footer_text--marginTop ]">
            Medlem av:
            <br />
            <b-img
              src="~/assets/images/akupunkturforeningen.svg"
              class="[ footer_logo footer_logo--small ]"
              alt="Logo Akupunkturforeningen"
              title="Logo Akupunkturforeningen"
            ></b-img>
          </p>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
import primaryBtnOutline from '~/components/buttons/primaryBtnOutline'

export default {
  components: {
    primaryBtnOutline
  }
}
</script>

<style lang="scss" scoped>
p,
h4 {
  color: $white;

  @media screen and (max-width: 990px) {
    text-align: center;
  }
}
.primarybtn {
  @media screen and (max-width: 990px) {
    display: block;
    margin: 0 auto;
  }
}

.footer {
  &_logo {
    @media screen and (max-width: 990px) {
      width: 290px;
      margin: 0 auto;
      padding-bottom: 20px;
      display: block;
    }

    &--small {
      @media screen and (max-width: 990px) {
        margin-top: 20px;
      }
    }
  }
  &_btn {
    @media screen and (max-width: 990px) {
      display: block;
      margin: 0 auto;
    }
  }

  &_container {
    background-color: $secondary;
    padding: 50px 0px;
  }

  &_colunm {
    padding-left: 50px;

    @media screen and (max-width: 990px) {
      padding-left: 0px;
    }
  }

  &_header {
    text-transform: uppercase;
    font-weight: 400;
    font-size: 16px;
    letter-spacing: 0.6px;
    margin-bottom: 5px;

    @media screen and (max-width: 990px) {
      margin-top: 20px;
    }

    &--marginTop {
      margin-top: 27px;

      @media screen and (max-width: 990px) {
        margin-top: 20px;
      }
    }
  }

  &_text {
    font-size: 14px;
    font-weight: 300;
    letter-spacing: 0.4px;

    &--right {
      padding-left: 30px;
    }

    &--marginTop {
      margin-top: 100px;

      @media screen and (max-width: 990px) {
        margin-top: 30px;
      }
    }

    &--extra {
      padding-left: 33px;
    }
  }
}
</style>
