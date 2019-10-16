<template>
  <div>
    <b-navbar toggleable="md" class="[ navheader_container ]">
      <b-navbar-bran to="/"><img src="/assets/images/zenter-hvit.svg" class="[ navheader_logo ]" alt="Kitten">zenter</b-navbar-bran>
      
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse class="[ navheader_container--dropdown ]" id="nav-collapse" is-nav>
        <b-navbar-nav class="[ navheader_list ]">
          <b-nav-item to="/akupunktur" class="[ navheader_listitem ]">Om Akupunktur</b-nav-item>
          <b-nav-item to="/plager" class="[ navheader_listitem ]">Plager</b-nav-item>
          <b-nav-item to="/behandlinger" class="[ navheader_listitem ]">Behandlinger</b-nav-item>
          <b-nav-item to="/kontakt" class="[ navheader_listitem ]">Kontakt</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<script>
export default {}
</script>

<style lang="scss" scope>
.navbar-toggler {
  display: none;
}
.navheader{
  &_logo{
    height: 40px;
    width: auto;
    position: absolute;
    left:20px;

  }
  &_list{
    position: absolute;
    right: 20px;
    @media screen and (max-width:768px) {
      position: relative;
    }
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
  &_container{
    margin: 0;
    padding:10px;
    background-color: rgba($secondary, .6);

    &--dropdown{
      background-color:$secondary;
      @media screen and (max-width:768px) {
       height: 100vh;
      }
    }
    }
}
</style>
