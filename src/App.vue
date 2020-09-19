<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/kof-icon.svg" />
    <KofHr hr-height="2px" hr-margin="1rem"/>
    <ExperimentOne  change-color-msg="Click me to change color" />
    <KofHr hr-height="2px" hr-margin="1rem"/>
    <ExperimentTwo nameish="Gal" job="Cosmic lover" my-strenth="Soft"/>
    <ExperimentTwo nameish="Chibi" job="Dog" my-strenth="Hard"/>
    <ExperimentTwo nameish="Luise" job="Cat" my-strenth="Pink"/>
    <ExperimentTwo />
  </div>
</template>

<script>
import ExperimentOne from "./components/ExperimentOne";
import ExperimentTwo from "./components/ExperimentTwo";
import KofHr from "./components/KofHr";

export default {
  name: "App",
  components: {
    ExperimentOne,
    ExperimentTwo,
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
