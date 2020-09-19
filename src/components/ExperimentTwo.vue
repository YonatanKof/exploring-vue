<template>
  <div class="hiyo">
    <h4>{{ myKofIs(strenth) }}</h4>
    <p>Hi {{ name }} the date & time now is {{ date('en-IL') }} and you are a {{ job }}</p>
  </div>
</template>

<script>
export default {
  name: "ExperimentTwo",
  props: {
    nameish: {
      type: String,
      default: "Yonatan",
    },
    job: {
      type: String,
      default: "a full retard",
    },
    myStrenth: {
      type: String,
      default: "Hard",
    },
  },
  methods: {
    myKofIs: function () {
      return (
        "My Kof is " + this.myStrenth + ", so say's " + this.nameish
      );
    },
    // myKofIs: function (myStrenth) {
    //   return "My Kof is " + myStrenth + " and he gos by the name of " + this.nameish;
    // },
    // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat/DateTimeFormat
    date(contry) {
      let theDate = new Date(Date());
      var options = {
        // calendar: "hebrew",
        // hour12: true,
        // dayPeriod: "short",
        // era: "short",
        // second: "numeric",
        hour: "numeric",
        minute: "numeric",
        // weekday: "short",
        day: "numeric",
        month: "short",
        // year: "2-digit",
        // timeZoneName: "long",
      };
      theDate = Intl.DateTimeFormat(contry, options).format(theDate);
      return theDate;
    },
  },
};
</script>

<style lang="scss" scoped>
div {
  text-align: left;
}
</style>
