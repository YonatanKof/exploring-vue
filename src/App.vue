<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/kof-icon.svg" />
    <experimentOne  change-color-msg="Click me to change color" />
  </div>
</template>

<script>
import experimentOne from "./components/experimentOne.vue";

export default {
  name: "App",
  components: {
    experimentOne,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333;
  margin-top: 60px;
}
</style>
