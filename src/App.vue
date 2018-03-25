<template>
  <div id="app">
    <v-header></v-header>
    <!--<router-view/>-->
  </div>
</template>

<script>
import header from './components/common/Header'

export default {
  name: 'App',
  components: {
    vHeader: header
  }
}
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin: 0;
    padding: 0;
  }
</style>
