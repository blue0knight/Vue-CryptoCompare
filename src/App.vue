<template>
  <div id="app">
    <img src="./assets/logo.png">
    <crypto></crypto>
  </div>
</template>

<script>

import Crypto from './components/Crypto'

export default {
  name: 'App',
  components: {
    Crypto
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
  margin-top: 60px;
}
</style>
