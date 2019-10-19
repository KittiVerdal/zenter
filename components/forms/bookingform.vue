<template>
  <div>
    <b-container fluid class="[ form_container ]">
      <b-container>
        <b-row>
          <b-col>
            <h2>
              Book time. Send inn skjema
              <br />og få time tilsendt på telefon
            </h2>
            <p>Du får tilsendt time så snart vi kan, dersom vi ikke har time tilgjengelig på ønsket tidspunktet tar vi kontakt med deg.</p>
            <p>*Må fylles ut</p>
          </b-col>
        </b-row>
        <b-row>
          <b-col md="6">
            <b-form inline>
              <label class="sr-only" for="inline-form-input-navn">Navn</label>
              <b-input id="navn" v-model="form.navn" required placeholder="Navn"></b-input>
              <label class="sr-only" for="inline-form-input-etternavn">Etternavn</label>
              <b-input id="navn" v-model="form.etternavn" required placeholder="Etternavn"></b-input>
            </b-form>
            <b-form inline>
              <label class="sr-only" for="inline-form-input-telefon">Telefon</label>
              <b-input id="telefon" v-model="form.telefon" required placeholder="Telefonnummer"></b-input>
              <label class="sr-only" for="inline-form-input-email">E-post</label>
              <b-input id="email" v-model="form.email" required placeholder="Email"></b-input>
            </b-form>
            <b-form inline>
              <label class="sr-only" for="inline-form-input-datofra">Dato fra</label>
              <b-input id="datoFra" v-model="form.datofra" required placeholder="Dato fra"></b-input>
              <label class="sr-only" for="inline-form-input-datotil">Dato til</label>
              <b-input id="datoTil" v-model="form.datoTil" required placeholder="Dato til"></b-input>
            </b-form>
            <b-button type="submit" variant="primary">Submit</b-button>
          </b-col>
        </b-row>
      </b-container>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: '',
        name: '',
        food: null,
        checked: []
      },
      foods: [
        { text: 'Select One', value: null },
        'Carrots',
        'Beans',
        'Tomatoes',
        'Corn'
      ],
      show: true
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
    }
  }
}
</script>

<style lang="scss" scoped>
.form {
  &_container {
    background-color: $secondaryDark;
  }
}
</style>