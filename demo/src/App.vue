<template>
  <div id="app">
    <linkModule></linkModule>
  </div>
</template>

<script>
import linkModule from 'link-module'

export default {
  name: 'app',
  components: {
    linkModule
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
