<template>
  <div>
    <b-navbar toggleable="lg" class="[ navheader--background ]">
      <b-navbar-bran class="[ navheader_logo ]">
          <nuxt-link to="/">Zenter</nuxt-link>
        </b-navbar-bran>
      
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="[ navheader_list ]">
          <b-nav-item class="[ navheader_listitem ]"
            ><nuxt-link to="akupunktur">Om Akupunktur</nuxt-link></b-nav-item
          >
          <b-nav-item class="[ navheader_listitem ]"
            ><nuxt-link to="plager">Plager</nuxt-link></b-nav-item
          >
          <b-nav-item class="[ navheader_listitem ]"
            ><nuxt-link to="behandlinger">Behandlinger</nuxt-link></b-nav-item
          >
          <b-nav-item class="[ navheader_listitem ]">
              <nuxt-link to="kontakt">Kontakt</nuxt-link></b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<script>
export default {}
</script>

<style lang="sass">
.navheader{
  &--background{
    margin: 0;
    padding:10px
    background-color: rgba($secondaryDark, .6)
  }
}
</style>
