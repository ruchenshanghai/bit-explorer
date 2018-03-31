<template>
  <div id="app">
    <v-header></v-header>
    <div id="content-div">
      <latest-block></latest-block>
      <latest-transactions></latest-transactions>
    </div>
  </div>
</template>

<script>
import header from './components/Header'
import latestBlock from './components/LatestBlock'
import latestTransactions from './components/LatestTransactions'

export default {
  name: 'App',
  components: {
    vHeader: header,
    LatestBlock: latestBlock,
    LatestTransactions: latestTransactions
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
  #content-div {
    text-align: left;
    margin: 40px;
  }
</style>
