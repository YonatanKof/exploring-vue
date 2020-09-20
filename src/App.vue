<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/kof-icon.svg" />
    <KofHr hr-height="2px" hr-margin="1rem" />
    <ExperimentOne change-color-msg="Click me to change color" />
    <KofHr hr-height="2px" hr-margin="1rem" />
    <ExperimentTwo />
    <ExperimentTwo
      nameish="Gal"
      job="Cosmic lover"
      my-strenth="Soft"
      social-link="https://www.w3schools.com/html/html_links.asp"
      my-html="<ul><li>Ponit one</li><li>2nd point</li><li>Last point</li></ul>"
    />
    <ExperimentTwo
      nameish="Chibi"
      job="Dog"
      my-strenth="Hard"
      social-link="https://github.com/you-dont-need/You-Dont-Need-Lodash-Underscore"
      my-html="<h2>Hi there!</h2>"
    />
    <ExperimentTwo
      nameish="Luise"
      job="Cat"
      my-strenth="Pink"
      social-link="https://heroicons.com/"
      my-html='<code style="font-size: 200%; color: red;">Hi there!</code>'
    />
  </div>
</template>

<script>
import ExperimentOne from "./components/ExperimentOne.vue";
import ExperimentTwo from "./components/ExperimentTwo.vue";
import KofHr from "./components/KofHr.vue";

export default {
  name: "App",
  components: {
    ExperimentOne,
    ExperimentTwo,
    KofHr,
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
