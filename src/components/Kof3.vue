<template>
  <div>
    <h1>{{ count }}</h1>
    <button class="kof"></button>
    <button class="kof"></button>
  </div>
</template>

<script>
export default {
  name: "Kof3",
  props: {
    count: {
      type: Number,
      default: 12,
    },
  },
};
</script>