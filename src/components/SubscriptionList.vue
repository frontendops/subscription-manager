<template>
  <div>
    <Datepicker calendar-class="cl-date" :disabled-dates="dates"/>
  </div>
</template>

<script>
import Datepicker from "vuejs-datepicker";
export default {
  components: {
    Datepicker
  },
  name: "SubscriptionList",
  data() {
    return {
      dates: {
        days: [6, 0],
        to: new Date(2019, 5, 4),
        from: new Date(2019, 5, 26)
      }
    };
  }
};
</script>

<style lang="css">
.cl-date {
  background: #fff;
}
</style>

