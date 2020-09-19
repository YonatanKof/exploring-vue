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
  },
  computed: {
    cssVars() {
      return {
        "--hr-height": this.hrHeight,
        "--hr-margin": this.hrMargin,
      };
    },
  },
};
</script>

<style>
hr {
  border: var(--hr-height) solid var(--color-system);
  border-radius: var(--hr-height);
  margin-top: var(--hr-margin);
  margin-bottom: var(--hr-margin);
}
</style>