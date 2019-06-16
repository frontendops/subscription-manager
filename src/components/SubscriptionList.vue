<template>
  <!-- make this a scoped slot -->
  <div>
    <h1>{{ title }}</h1>
    <div role="list">
      <Subscription
        v-for="(item, index) in subscriptions"
        :key="index"
        :title="item.name"
        :price="item.price"
      />
    </div>
  </div>
</template>

<script>
import Subscription from "./Subscription";
export default {
  components: {
    Subscription
  },
  name: "SubscriptionList",
  data() {
    return {
      title: "your subscriptions",
      subscriptions: [
        {
          name: "Netflix",
          price: 10
        },
        {
          name: "Spotify",
          price: 10
        },
        {
          name: "Medium",
          price: 10
        },
        {
          name: "Netflix",
          price: 10
        }
      ]
    };
  }
};
</script>

<style lang="css">
.cl-date {
  background: #fff;
}
</style>

