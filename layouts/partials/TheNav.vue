<template>
  <div>
    <b-navbar toggleable="md" class="[ navheader navheader_container ]">
      <nuxt-link to="/">
        <img
          src="~/assets/images/zenter-hvit.svg"
          class="[ navheader_logo ]"
          alt="Logoen til Zenter Akupunkturklinikk"
          title="Logoen til Zenter Akupunkturklinikk"
        />
      </nuxt-link>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="[ navheader_list ]">
          <b-nav-item to="/">Hjem</b-nav-item>
          <b-nav-item to="/plager">Plager</b-nav-item>
          <b-nav-item to="/behandlinger">Behandlinger</b-nav-item>
          <b-nav-item to="/priser">Priser</b-nav-item>
          <b-nav-item to="/kontakt">Kontakt</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<script>
export default {}
</script>

<style lang="scss" scope>
.navbar {
  z-index: 100;
}

.navbar-toggler {
  display: none;
}
.navheader {
  height: 80px;
  &_logo {
    height: 60px;
    width: auto;
    position: fixed;
    left: 20px;
    top: 10px;
    z-index: 100;
  }
  &_list {
    position: absolute;
    right: 20px;
    @media screen and (max-width: 768px) {
      position: relative;
    }
  }
  &_container {
    margin: 0;
    padding: 10px;
    background-color: rgba($secondaryDark, 0.7);
    position: fixed;
    width: 100%;
  }
}
.navbar-light .navbar-nav .nav-link {
  color: $white;
  font-family: $zenterfont;
  padding: 20px;
  letter-spacing: 0.6px;
  font-weight: 400;
  z-index: 101;
  font-size: 18px;
  &:hover {
    color: $secondaryLight;
    text-decoration: none;
  }
  &:active {
    color: $secondaryLight;
    text-decoration: none;
  }
  &:focus {
    color: $secondaryLight;
    text-decoration: none;
  }
}
</style>
