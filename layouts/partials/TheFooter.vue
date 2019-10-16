<template>
<b-container fluid class="[ footer_container ]">
<b-container>
  <b-row>
    <b-col md="2"><b-img src="~/assets/images/zenter.svg" class="[ footer_logo ]" alt="Zenter Akupunkturklinikk logo" title="Zenter Akupunkturklinikk logo"></b-img></b-col>
    <b-col md="4">
        <h4>Åpningstider</h4>
        <p>Mandag:<span>07:00 - 19:00</span><br>
        Tirsdag:<span>07:00 - 19:00</span><br>
        Torsdag:<span>07:00 - 19:00</span><br>
        Onsdag og fredag åpent etter avtale</p>
        <p>Telefontid alle hverdager fra 08:00-16:00<br>Avbestilling av timer kun pr telefon.</p>
        </b-col>
    <b-col md="3">
        <h4>Telefon 905 56 932</h4>
        <h4>Adresse</h4>
        <p>Kjøpmannsbrotet 5,<br>4351 Kleppe</p>
        <p><b-link href="#foo">Åpne adresse i Google maps her»</b-link></p>
    </b-col>
    <b-col md="3">
        <b-button>Admin log in</b-button>
        <p>Medlem av:<br>
        <b-img src="~/assets/images/akupunkturforeningen.svg" class="[ footer_logo ]" alt="Logo Akupunkturforeningen" title="Logo Akupunkturforeningen"></b-img></p>
        
    </b-col>
  </b-row>
</b-container>
</b-container>
</template>
    
<script>
export default {
    
}
</script>

<style lang="scss" scoped>
p,h4 {
    color:$white;
}
.footer{
    &_container{
        background-color: $secondary;
        padding:40px 0px;
    }
}

</style>