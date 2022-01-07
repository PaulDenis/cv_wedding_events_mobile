<template>
  <div id="app">
    <Header />
    <BrandDesc />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import BrandDesc from './components/BrandDesc.vue'

export default {
  name: 'App',
  components: {
    Header,
    BrandDesc
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
