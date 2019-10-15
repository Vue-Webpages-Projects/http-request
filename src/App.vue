<template>
  <div id="app">
    <GETRequest />
  </div>
</template>

<script>
import GETRequest from './components/GETRequest.vue'

export default {
  name: 'app',
  components: {
    GETRequest
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
