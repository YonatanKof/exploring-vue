<template>
  <main id="app">
    <img alt="Vue logo" src="./assets/kof-icon.svg" />
    <KofHr hr-margin="2rem" />
    <ToDo />
    <KofHr hr-margin="2rem" hr-color="red" />
    <Kof1 change-color-msg="Click me to change color" main-msg="Kof me hard in arss"/>
    <KofHr hr-height="1rem" hr-margin="4rem" hr-color="#d6d6d6" />
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
      my-html="<code style='font-size: 200%; color: red;'>Hi there!</code>"
    />
    <KofHr hr-margin="4rem" />
    <Kof3 />
    <KofHr hr-margin="4rem" />
    <Kof4 />
    <h1>Kof 2</h1>
    <Kof5 />
  </main>
</template>

<script>
import Kof1 from "./components/Kof1.vue";
import Kof2 from "./components/Kof2.vue";
import Kof3 from "./components/Kof3.vue";
import Kof4 from "./components/Kof4.vue";
import Kof5 from "./components/Kof5.vue";
import ToDo from "./components/ToDo.vue";
import KofHr from "./components/KofHr.vue";

export default {
  name: "App",
  components: {
    Kof1,
    Kof2,
    Kof3,
    Kof4,
    Kof5,
    ToDo,
    KofHr,
  },
};
</script>

<style lang="scss">
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
button, input {
  font-size: 0.8rem;
  padding: 0.7em 1em;
  border-radius: 0.4em;
  border: none;
  background-color: lightblue;
  &:not(:first-child) {
    margin-inline-start: 0.8em;
  }
}
input{
  background-color: lightgoldenrodyellow;
}
</style>
