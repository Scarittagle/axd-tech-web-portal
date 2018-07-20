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
  @import '~bulma'
  @import './assets/styles/custom-style'
  @import "~buefy/src/scss/buefy"
  @font-face
    font-family: shanhun
    src: url('/static/font/shanhun.ttf')
  @font-face
    font-family: Bahnschrift
    src: url('/static/font/bahnschrift.ttf')
  @font-face
    font-family: "Microsoft JhengHei UI"
    src: url('/static/font/msjh.ttc')

  #app
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    color: #2c3e50
</style>
