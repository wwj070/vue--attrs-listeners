<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <directive />
    <!-- <HelloWorld /> -->
  </div>
</template>

<script>
import HelloWorld from './HelloWorld'
import directive from './directive'

export default {
  name: 'App',
  components: {
    HelloWorld, directive
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
  font-size: 16px;
}
</style>
