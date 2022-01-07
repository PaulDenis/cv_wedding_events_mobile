<template>
  <div id="app">
    <Header @lingua="lingua"/>
    <BrandDesc 
    :linguaggio="linguaggio"/>
    <LandingCarousel 
    :linguaggio="linguaggio"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import BrandDesc from './components/BrandDesc.vue'
import LandingCarousel from './components/LandingCarousel.vue'

export default {
  name: 'App',
  components: {
    Header,
    BrandDesc,
    LandingCarousel
  },
  data() {
    return {
      linguaggio: 'inglese'
    }
  },
  methods: {
    lingua: function(lingua) {
      this.linguaggio = lingua;
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

</style>
