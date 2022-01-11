<template>
  <div id="app">
    <div class="home" v-if="pagina_corrente == 'home'">
      <NavBar
      @pagina="pagina"
      :linguaggio="linguaggio"/>
      <Header 
      @lingua="lingua"/>
      <PersonalDesc 
      :linguaggio="linguaggio"/>
      <LandingCarousel 
      :linguaggio="linguaggio"/>
      <BrandDesc 
      :linguaggio="linguaggio"/>
      <Footer 
      :linguaggio="linguaggio"/>
    </div>
    <div class="about_us" 
    v-if="pagina_corrente == 'about us'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"/>
      <Manutenzione :linguaggio="linguaggio"/>
    </div>
    <div class="about_us" 
    v-if="pagina_corrente == 'galleria'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"/>
      <Manutenzione :linguaggio="linguaggio"/>
    </div>
    <div class="about_us" 
    v-if="pagina_corrente == 'contatti'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"/>
      <Manutenzione :linguaggio="linguaggio"/>
    </div>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Header from './components/Header.vue'
import BrandDesc from './components/BrandDesc.vue'
import LandingCarousel from './components/LandingCarousel.vue'
import PersonalDesc from './components/PersonalDesc.vue'
import Footer from './components/Footer.vue'
import Manutenzione from './components/Manutenzione.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    Header,
    BrandDesc,
    LandingCarousel,
    PersonalDesc,
    Footer,
    Manutenzione
  },
  data() {
    return {
      linguaggio: 'inglese',
      pagina_corrente: 'home'
    }
  },
  methods: {
    lingua: function(lingua) {
      this.linguaggio = lingua;
    },
    pagina: function(pagina) {
      this.pagina_corrente = pagina;
    }
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}


@import'~bootstrap/dist/css/bootstrap.css';
</style>
