<template>
  <div id="app">
    <app-navbar/>
    <router-view/>
    <app-footer/>
  </div>
</template>

<script>
  import Navbar from './components/layout/Navbar';
  import Footer from './components/layout/Footer';

  export default {
    name: 'App',
    components: {
      'app-navbar': Navbar,
      'app-footer': Footer,
    },
  }
</script>

<style lang="sass">
  @import "~bulma"
  @import "~buefy/src/scss/buefy"
  @font-face
    font-family: shanhun
    src: url('/static/font/shanhun.ttf')

  #app
    font-family: 'DengXian';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
</style>
