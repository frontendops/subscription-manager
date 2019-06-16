<template>
  <!-- make this a scoped slot -->
  <div>
    <h1>{{ title }}</h1>
    <div role="list" class="subscription-list">
      <Subscription
        v-for="(item, index) in subscriptions"
        :key="index"
        :title="item.name"
        :price="item.price"
        :color="item.color"
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
      title: "Your subscriptions",
      subscriptions: [
        {
          name: "Netflix",
          price: 10,
          color: "#e31929"
        },
        {
          name: "Spotify",
          price: 10,
          color: "#028858"
        },
        {
          name: "Medium",
          price: 5,
          color: "#024c8e"
        },
        {
          name: "Headspace",
          price: 12,
          color: "#f9af2f"
        }
      ]
    };
  }
};
</script>

<style lang="css">
.subscription-list {
  margin: 0 auto;
  max-width: 900px;
  padding: 0 8px;
}
</style>

