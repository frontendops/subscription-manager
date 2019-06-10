<template>
  <div class="home">
    <SubscriptionList/>
  </div>
</template>

<script>
import SubscriptionList from "./SubscriptionList";
export default {
  components: {
    SubscriptionList
  },
  name: "Home",
  props: {
    msg: String
  }
};
</script>

<style scoped>
.home {
  height: 100vh;
  width: 100vw;
  background-color: #eeeeee;
  padding: 16px;
}
</style>
