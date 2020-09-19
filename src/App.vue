<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/kof-icon.svg">
    <ChangeCss msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import ChangeCss from './components/ChangeCss.vue'

export default {
  name: 'App',
  components: {
    ChangeCss
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
