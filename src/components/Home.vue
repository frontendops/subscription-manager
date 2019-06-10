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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home {
  height: 100vh;
  width: 100vw;
  background-color: #eeeeee;
}
</style>
