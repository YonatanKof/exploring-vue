<template>
  <main>
    <h1>Kof 3</h1>
    <div id="one-way">
      <h3>Count inline: {{ countOne }}</h3>
      <div>
        <button id="kof-btn" v-on:click="countOne++">Add from number</button>
        <button v-on:click="countOne--">Remove from nubmer</button>
      </div>
    </div>
    <div id="another-way">
      <h3>Counting w/ a function: {{ countTwo }}</h3>
      <div>
        <button v-on:click="add(1)">Add from number</button>
        <button v-on:dblclick="add(10)">DBLC+10</button>
        <button v-on:click="remove(1)">Remove from nubmer</button>
        <button v-on:dblclick="remove(10)">DBLC-10</button>
      </div>
    </div>
    <div class="board" v-on:mousemove="updatePosition">{{ x }}, {{ y }}</div>
  </main>
</template>

<script>
export default {
  name: "Kof3",
  props: {
    // countOne: {
    //   type: Number,
    //   default: 12,
    // },
    // countTwo: {
    //   type: Number,
    //   default: 12,
    // },
    // x: {
    //   type: Number,
    //   default: 300,
    // },
    // y: {
    //   type: Number,
    //   default: 250,
    // },
  },
  data() {
    return {
      countOne: 12,
      countTwo: 12,
      x: 300,
      y: 250,
    };
  },
  methods: {
    add(inc) {
      this.countTwo += inc;
    },
    remove(dec) {
      this.countTwo -= dec;
    },
    updatePosition: function (event) {
      // console.log(event);
      this.x = event.offsetX;
      this.y = event.offsetY;
    },
  },
};
</script>

<style lang="scss">
.board {
  color: white;
  font-weight: 900;
  font-size: 3rem;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 600px;
  // width: 90vw;
  height: 500px;
  margin: 2rem auto;
  border-radius: 1rem;
  border: 0.2em solid dodgerblue;
  background: radial-gradient(
      at bottom right,
      dodgerblue 0,
      dodgerblue 1em,
      lightskyblue 1em,
      lightskyblue 2em,
      deepskyblue 2em,
      deepskyblue 3em,
      gainsboro 3em,
      gainsboro 4em,
      lightsteelblue 4em,
      lightsteelblue 5em,
      deepskyblue 5em,
      deepskyblue 6em,
      lightskyblue 6em,
      lightskyblue 7em,
      transparent 7em,
      transparent 8em
    ),
    radial-gradient(
      at top left,
      transparent 0,
      transparent 1em,
      lightskyblue 1em,
      lightskyblue 2em,
      deepskyblue 2em,
      deepskyblue 3em,
      lightsteelblue 3em,
      lightsteelblue 4em,
      gainsboro 4em,
      gainsboro 5em,
      deepskyblue 5em,
      deepskyblue 6em,
      skyblue 6em,
      skyblue 7em,
      dodgerblue 7em,
      dodgerblue 8em,
      transparent 8em,
      transparent 20em
    ),
    radial-gradient(circle at center bottom, coral, darkslateblue);

  background-blend-mode: overlay;
  background-size: 8em 8em, 8em 8em, cover;
}
</style>