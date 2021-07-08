<template>
  <div id="app">
    <Header/>
    <Vetrina/>
  </div>
</template>

<script>
import Vetrina from './components/Vetrina.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,
    Vetrina
  }
}
</script>

<style lang="scss">
@import '@/style/general.scss';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
