<template>
  <!-- make this a scoped slot -->
  <div>
    <h1>{{ title }}</h1>
    <div class="total-price">
      <span>Your Total</span>
      <span class="lines"></span>
      <span class="total-price__total">${{total}}</span>
    </div>
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
      total: null,
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
  },
  methods: {
    getTotal() {
      let prices = [];
      let sum;
      this.subscriptions.forEach(subscription =>
        prices.push(subscription.price)
      );
      sum = prices.reduce((a, b) => a + b);
      this.total = sum;
    }
  },
  mounted() {
    this.getTotal();
  }
};
</script>

<style lang="css">
.subscription-list {
  margin: 0 auto;
  margin-top: 16px;
  max-width: 900px;
  padding: 0 8px;
}

.total-price {
  display: flex;
  font-size: 2rem;
  max-width: 900px;
  justify-content: space-between;
  margin: 0 auto;
  padding: 0 8px;
}

.total-price__total {
  font-weight: bold;
}

.lines {
  border-bottom: 2px dotted black;
  flex-grow: 1;
}
</style>

