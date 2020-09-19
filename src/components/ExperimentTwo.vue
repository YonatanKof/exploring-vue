<template>
  <div>
    <h3>{{ name }}</h3>
    <h3>{{ job }}</h3>
  </div>
</template>

<script>
export default {
  name: "ExperimentTwo",
  props: {
    name: {
      default: "Yonatan Kof",
      type: String,
    },
    job: {
      default: "Designer",
      type: String,
    }
  },
};
</script>

<style lang="scss">
</style>
