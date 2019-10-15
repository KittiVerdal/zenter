<template>
  <div>
    <b-navbar toggleable="md" class="[ navheader--background ]">
      <b-navbar-bran class="[ navheader_logo ]">
          <nuxt-link to="/">Zenter</nuxt-link>
        </b-navbar-bran>
      
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" class="[ navheader_dropdown ]" is-nav>
        <b-navbar-nav class="[ navheader_list ]">
          <b-nav-item href=""><nuxt-link to="akupunktur" class="[ navheader_listitem ]">Om Akupunktur</nuxt-link></b-nav-item>
          <b-nav-item href=""><nuxt-link to="plager" class="[ navheader_listitem ]">Plager</nuxt-link></b-nav-item>
          <b-nav-item href=""><nuxt-link to="behandlinger" class="[ navheader_listitem ]">Behandlinger</nuxt-link></b-nav-item>
          <b-nav-item href=""><nuxt-link to="kontakt" class="[ navheader_listitem ]">Kontakt</nuxt-link></b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<script>
export default {}
</script>

<style lang="scss" scope>
.navheader{
  &_logo{
    height: 40px;
  }
  &_list{
    position: absolute;
    right:20px;
  }
  &_listitem{
    color: $white;
    font-family: $zenterfont;
    padding:15px;
    letter-spacing: 0.6px;
    font-weight: 400;

    &:hover{
      color: $secondaryLight;
      text-decoration: none;
    }
  }
  &_dropdown{
    background-color: rgba($secondary, .6);
  }
  &--background{
    margin: 0;
    padding:10px;
    background-color: rgba($secondary, .6);
    height: 60px;
   }
}
</style>
