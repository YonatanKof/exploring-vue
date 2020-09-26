<template>
  <hr :style="cssVars"/>
</template>

<script>
export default {
  name: "KofHr",
  props: {
    hrHeight: {
      default: "1px",
      type: String,
    },
    hrMargin: {
      default: "1rem",
      type: String,
    },
    hrColor: {
      default: "var(--color-system)",
      type: String,
    },
  },
  computed: {
    cssVars() {
      return {
        "--hr-height": this.hrHeight,
        "--hr-margin": this.hrMargin,
        "--hr-color": this.hrColor,
      };
    },
  },
};
</script>

<style>
hr {
  border: var(--hr-height) solid var(--hr-color);
  border-radius: var(--hr-height);
  margin-top: var(--hr-margin);
  margin-bottom: var(--hr-margin);
}
</style>