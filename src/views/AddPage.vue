<template>
  <div class="addPage">
    Enter Subscription
    <form action="post">
      <input type="text" placeholder="Name">
      <input type="number" name="price" id="price" min="1" step="1">
      <!-- insert datepicker library -->

      <input type="submit">
    </form>
  </div>
</template>

<script>
export default {
  name: "AddPage"
};
</script>

<style scoped>
.addPage {
  text-align: center;
}
</style>
