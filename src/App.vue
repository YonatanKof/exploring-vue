<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/kof-icon.svg" />
    <KofHr hr-height="2px" hr-margin="1rem"/>
    <experimentOne  change-color-msg="Click me to change color" />
    <KofHr hr-height="2px" hr-margin="1rem"/>
    <experimentTwo/>
  </div>
</template>

<script>
import experimentOne from "./components/experimentOne.vue";
import experimentTwo from "./components/experimentTwo.vue";
import KofHr from "./components/KofHr";

export default {
  name: "App",
  components: {
    experimentOne,
    experimentTwo,
    KofHr
  },
};
</script>

<style>
:root {
  font-size: 16px;
  --title-1: 4rem;
  --title-3: 3rem;
  --color-system: #333;
  --color-caution: red;
  --color-success: blue;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333;
  margin-top: 60px;
}
</style>
