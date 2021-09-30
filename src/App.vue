<template>
  <div id="app">
    <Header />
    <SongsPreview />
  </div>
</template>

<script>
import SongsPreview from './components/SongsPreview.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,
    SongsPreview,
  }
}
</script>

<style lang="scss">
@import "./style/variables.scss";
@import "./style/general.scss";

#app {


  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
