<template>
  <div class="hiyo">
    <h1>{{ myKofIs(strenth) }}</h1>
    <p>Hi {{ name }} the date & time now is {{ date('en-IL') }} and you are a {{ job }}.</p>
    <p>
      You can 
      <a target="_blank" v-bind:href="socialLink">find me online here</a>
    </p>
    <p v-html="myHtml"></p>
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
      default: "a Full retard",
    },
    socialLink: {
      type: String,
      default: "https://exploring-vue.netlify.app/",
    },
    myHtml: {
      type: String,
      default: 'You can <a target="_blank" href="https://dribbble.com/yonatan_kof" >also find me here</a>',
    },
    myStrenth: {
      type: String,
      default: "Hard",
    },
  },
  methods: {
    myKofIs: function () {
      return "This is " + this.myStrenth + ", so say's " + this.nameish;
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
