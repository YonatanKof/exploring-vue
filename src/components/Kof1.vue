<template>
  <div class="hello">
    <h1>{{ mainMsg }}</h1>
    <div
      id="change-color"
      v-on:click="dange = !dange"
      v-bind:class="{kofClass: kofClass, dange: dange}"
    >
      <h3>{{ changeColorMsg }}</h3>
    </div>
    <div :class="compClasses">
      <div>
        <button v-on:click="titles = !titles">Toggle Color</button>
        <button v-on:click="extraTitles = !extraTitles">Toggle Width</button>
      </div>
      <h3>Hell yes</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "Kof1",
  props: {
    mainMsg: {
      default: "Hi stranger",
      type: String,
    },
    changeColorMsg: {
      default: "Change color here",
      type: String,
    },
  },
  data() {
    return {
      kofClass: true,
      dange: false,
      titles: false,
      extraTitles: false,
    };
  },
  computed: {
    compClasses: function () {
      return {
        titles: this.titles,
        extraTitles: this.extraTitles,
      };
    },
  },
};
</script>

<style lang="scss" scoped>
.kofClass {
  cursor: pointer;
  color: var(--color-success);
}
.dange {
  color: var(--color-caution);
}
h1 {
  font-size: var(--title-1);
}
h3 {
  font-weight: 100;
  font-size: var(--title-3);
  margin: 0.25em;
  transition: font-weight 0.5s, color 0.25s;
}
.titles {
  h3 {
    color: var(--color-caution);
  }
}
.extraTitles {
  h3 {
    font-weight: 900;
  }
}
</style>
