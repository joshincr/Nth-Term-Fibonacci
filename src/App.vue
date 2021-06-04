<template>
  <div id="app">
    <Fibonacci />
  </div>
</template>

<script>
import Fibonacci from './components/Fibonacci.vue';

export default {
  name: 'App',
  components: {
    Fibonacci
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
