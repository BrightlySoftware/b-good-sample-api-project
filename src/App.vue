<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <CatFacts/>
</template>

<script>
import CatFacts from './components/catfacts.vue'

export default {
  name: 'App',
  components: {
    CatFacts
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
