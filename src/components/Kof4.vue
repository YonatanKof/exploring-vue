<template>
  <main>
    <div id="example">
      <p>Original message: "{{ message }}"</p>
      <p>Computed reversed message: "{{ reversedMessage }}"</p>
    </div>
    <div id="another-way">
      <h3>Counting w/ a function: {{ countMe }}</h3>
      <div>
        <button v-on:click="add(20)">Add from number</button>
        <!-- <button v-on:dblclick="add(10)">DBLC+10</button>
        <button v-on:click="remove(1)">Remove from nubmer</button>
        <button v-on:dblclick="remove(10)">DBLC-10</button>-->
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "Kof4",
  data() {
    return {
      message: "YonatanKof",
      countMe: 12,
    };
  },
  methods: {
    add(inc) {
      this.countMe += inc;
    },
  },
  computed: {
    reversedMessage: function () {
      return this.message.split("").reverse().join("");
    },
  },
};
</script>
