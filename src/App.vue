<template>
  <div id="app">
    <Weekend />
    <TheFooter />
  </div>
</template>

<script>
import Weekend from './components/Weekend.vue'
import TheFooter from './components/TheFooter.vue'

export default {
  name: 'app',
  components: {
    Weekend,
    TheFooter
  }
}
</script>

<style>
body,
html {
  color: #ccc;
  background-color: #212226;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
