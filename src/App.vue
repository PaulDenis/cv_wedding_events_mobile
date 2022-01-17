<template>
  <div id="app">
    <div class="home" v-if="pagina_corrente == 'home'">
      <NavBar
      @pagina="pagina"
      :linguaggio="linguaggio"
      :pagina_corrente="pagina_corrente"/>
      <Header 
      @lingua="lingua"/>
      <BrandDesc 
      :linguaggio="linguaggio"/>
      <LandingCarousel 
      :linguaggio="linguaggio"/>
      <PersonalDesc 
      :linguaggio="linguaggio"/>
      <Footer 
      :linguaggio="linguaggio"/>
    </div>
    <div
    v-if="pagina_corrente == 'type of events'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"
      :pagina_corrente="pagina_corrente"/>
      <Manutenzione :linguaggio="linguaggio"/>
    </div>
    <div
    v-if="pagina_corrente == 'innovative ideas'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"
      :pagina_corrente="pagina_corrente"/>
      <Manutenzione :linguaggio="linguaggio"/>
    </div>
    <div
    v-if="pagina_corrente == 'about us'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"
      :pagina_corrente="pagina_corrente"/>
      <Manutenzione :linguaggio="linguaggio"/>
    </div>
    <div
    v-if="pagina_corrente == 'galleria'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"
      :pagina_corrente="pagina_corrente"/>
      <Manutenzione :linguaggio="linguaggio"/>
    </div>
    <div
    v-if="pagina_corrente == 'contatti'">
      <NavBar 
      @pagina="pagina"
      :linguaggio="linguaggio"
      :pagina_corrente="pagina_corrente"/>
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
      linguaggio: 'italiano',
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
