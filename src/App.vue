<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Score></Score>
  </div>
</template>

<script>
import Score from './components/score.vue'

export default {
  name: 'App',
  components: {
    Score
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
