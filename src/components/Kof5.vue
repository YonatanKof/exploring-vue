<template>
  <main>
    <div class="lists">
      <ul id="kof-list-1">
        <div v-for="item in items1" :key="item.id">
          {{ item }}
        </div>
      </ul>

      <ul id="kof-list-2">
        <div v-for="item in items2" :key="item.message">
          {{ item.message }}
        </div>
      </ul>

      <ul id="kof-list-3">
        <div v-for="(item, index) in items2" :key="item.message">
          {{ perMessage }} {{ item.message }}, {{ index }}
        </div>
      </ul>

      <ul id="kof-list-4">
        <div v-for="(item, title, index) in items3" :key="item">
          {{ title }}: {{ item }}, {{ index }}
        </div>
      </ul>

      <ul id="kof-list-even">
        <div v-for="n in evenNumber" :key="n">
          {{ n }}
        </div>
      </ul>

      <ul id="kof-list-odd">
        <div v-for="n in oddNumber" :key="n">
          {{ n }}
        </div>
      </ul>

      <ul id="kof-list-integer-range">
        <div v-for="n in 4" :key="n">
          {{ n }}
        </div>
      </ul>
    </div>
  </main>
</template>
<script>
export default {
  name: "Kof5",
  data() {
    return {
      perMessage: "All you need is ",
      items1: ["Love", "Hate", "Money", "Health"],
      items2: [
        { message: "Love" },
        { message: "Hate" },
        { message: "Money" },
        { message: "Health" },
      ],
      items3: {
        One: "Love",
        Two: "Hate",
        Three: "Money",
        Four: "Health",
      },
      numbers: [1, 2, 3, 4, 5],
    };
  },
  computed: {
    evenNumber() {
      return this.numbers.filter(function (number) {
        return number % 2 === 0;
      });
    },
    oddNumber() {
      return this.numbers.filter(function (number) {
        return number % 2 !== 0;
      });
    },
  },
};
</script>

<style scoped>
.lists {
  display: flex;
}
ul {
  margin: 0.5em 0;
  margin-inline-end: 1em;
  padding: 0;
  color: royalblue;
  text-align: left;
  font-size: 1.2rem;
}
</style>
