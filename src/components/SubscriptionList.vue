<template>
  <div>
    <Datepicker/>
    <Datepicker/>
    <Datepicker :inline="true" calendar-class="cl-date"/>
  </div>
</template>

<script>
import Datepicker from "vuejs-datepicker";
export default {
  components: {
    Datepicker
  },
  name: "SubscriptionList"
};
</script>

<style lang="scss" scoped>
</style>

