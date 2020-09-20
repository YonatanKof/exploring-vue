<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/kof-icon.svg" />
    <KofHr hr-height="2px" hr-margin="1rem" />
    <Kof1 change-color-msg="Click me to change color" />
    <KofHr hr-height="2px" hr-margin="1rem" />
    <Kof3 />
    <KofHr hr-height="2px" hr-margin="1rem" />
    <Kof2 />
    <Kof2
      nameish="Gal"
      job="Cosmic lover"
      my-strenth="Soft"
      social-link="https://www.w3schools.com/html/html_links.asp"
      my-html="<ul><li>Ponit one</li><li>2nd point</li><li>Last point</li></ul>"
    />
    <Kof2
      nameish="Chibi"
      job="Dog"
      my-strenth="Hard"
      social-link="https://github.com/you-dont-need/You-Dont-Need-Lodash-Underscore"
      my-html="<h2>Hi there!</h2>"
    />
    <Kof2
      nameish="Luise"
      job="Cat"
      my-strenth="Pink"
      social-link="https://heroicons.com/"
      my-html='<code style="font-size: 200%; color: red;">Hi there!</code>'
    />
  </div>
</template>

<script>
import Kof1 from "./components/Kof1.vue";
import Kof2 from "./components/Kof2.vue";
import Kof3 from "./components/Kof3.vue";
import KofHr from "./components/KofHr.vue";

export default {
  name: "App",
  components: {
    Kof1,
    Kof2,
    Kof3,
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
