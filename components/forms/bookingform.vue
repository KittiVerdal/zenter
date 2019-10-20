<template>
  <div>
    <b-modal id="modal-lg" size="lg" title="Timebestilling">
      <div class="[ modal_container ]">
        <h2 class="[ modal_headline ]">
          <span class="[ modal_headline--blue ]">Book time.</span>
          <br />Send inn skjema og få time tilsendt på telefon
        </h2>
        <p class="[ modal_bodyText ]">
          Normal responstid er innen 1 time. Du får tilsendt time så snart vi kan, dersom vi ikke har time
          tilgjengelig på ønsket tidspunktet tar vi kontakt med deg.
        </p>
        <p>*Må fylles ut</p>
        <b-form value:onSubmit>
          <b-form-group id="Treatment" label="Velg behandlingstype*:" label-for="treatment">
            <b-form-select
              id="treatment"
              v-model="form.treatment"
              :options="treatments"
              required
              class="[ form_inputfield ]"
            ></b-form-select>
          </b-form-group>
          <b-form-group id="Name" label-sr-only="Navn:*" label-for="firstname">
            <b-form-input
              id="firstname"
              v-model="form.name"
              required
              placeholder="Navn*"
              class="[ form_inputfield ]"
            ></b-form-input>
          </b-form-group>
          <b-form-group id="Phone" label-sr-only="Telefon:*" label-for="phone">
            <b-form-input
              id="phone"
              v-model="form.number"
              required
              placeholder="Telefonnummer*"
              class="[ form_inputfield ]"
            ></b-form-input>
          </b-form-group>
          <b-form-group id="Email" label-sr-only="E-post:" label-for="email">
            <b-form-input
              id="email"
              v-model="form.email"
              type="email"
              placeholder="Epost"
              class="[ form_inputfield ]"
            ></b-form-input>
          </b-form-group>
          <b-form-group id="DateFrom" label-sr-only="Fra Dato" label-for="dateFrom">
            <b-form-input
              id="datefrom"
              v-model="form.date"
              required
              placeholder="Ønker fra dato"
              class="[ form_inputfield ]"
            ></b-form-input>
          </b-form-group>
          <b-form-group id="DateTo" label-sr-only="Til Dato" label-for="dateTo">
            <b-form-input
              id="dateto"
              v-model="form.date"
              required
              date
              placeholder="Til dato"
              class="[ form_inputfield ]"
            ></b-form-input>
          </b-form-group>

          <b-form-group id="Time">
            <p class="[ modal_bodyText--small ]">Når passer det best for deg?</p>
            <b-form-checkbox-group v-model="form.checked" id="time">
              <b-form-checkbox value="07:00-11:00">kl. 07:00-11:00</b-form-checkbox>
              <b-form-checkbox value="02:00-15:00">kl. 12:00-15:00</b-form-checkbox>
              <b-form-checkbox value="15:00-18:00">kl. 15:00-18:00</b-form-checkbox>
              <b-form-checkbox value="Første tilgjengelige">Første tilgjengelige</b-form-checkbox>
            </b-form-checkbox-group>
          </b-form-group>
          <b-button class="[ buttonModal ]" type="submit" variant="primary">Submit</b-button>
        </b-form>
      </div>
      <template v-slot:modal-footer>
        <div></div>
      </template>
    </b-modal>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        treatment: '',
        name: '',
        date: '',
        date: '',
        email: '',
        number: null,
        checked: []
      },
      treatments: [
        { text: 'Velg en behandlingstype', value: null },
        'Akupunktur - førstegangskonsultasjon',
        'Akupunktur - oppfølging',
        'Kopping',
        'Kosmetisk akupunktur - Førstegangskonsultasjon',
        'Kosmetisk Akupunktur - Oppfølgingstime',
        'Elektroakupunktur',
        'Guasha',
        'Kombi: Akupunktur + Kopping',
        'Kombi: Akupunktur + Triggerpunkt',
        'Kombi: Akupunktur + Triggerpunkt + Kopping',
        'Moxa varmebehandling',
        'Ørelysbehandling'
      ],
      show: true
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      console.log(JSON.stringify(this.form))
    }
  }
}
</script>

<style lang="scss" scoped>
h5 {
  text-transform: uppercase;
}
.modal {
  &_container {
    padding-left: 20px;
    padding-right: 20px;
  }
  &_headline {
    font-family: $zenterfont;
    font-weight: 600;
    font-size: 28px;
    color: $secondary;
    &--blue {
      color: $primary;
      font-size: 50px;
    }
  }
  &_bodyText {
    color: $greyDark;
  }
}
.form {
  &_container {
    font-family: $zenterfont;
  }
  &_inputfield {
    border-radius: 50px;
    border: 1px solid rgba($primary, 0.5);
  }
}

.buttonModal {
  display: inline-block;
  padding: 10px;
  border: 2px solid $primary;
  border-radius: 3px;
  background-color: transparent;
  color: $primary;
  font-family: $zenterfont;
  border-radius: 50px;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.8px;
  line-height: 1;
  width: 120px;
  margin-top: 20px;
  text-decoration: none;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.4s;

  &:hover {
    background: $primary;
    color: #fff;
    box-shadow: 0px 3px 30px 0px rgba($primary, 0.5);
    transition: 0.3s;
  }
}
</style>