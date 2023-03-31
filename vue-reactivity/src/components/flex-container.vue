<template>
  <div class="main">
    <div class="first-el">
      <productCard></productCard>
    </div>
    <div class="second-el">
      <h2>Cart</h2>
    </div>
  </div>
</template>

<script>
import productCard from "./product-card.vue";
export default {
  name: "kuntainer",
  components: {
    productCard,
  },
};
</script>

<style scoped>
.main {
  display: flex;
}
.first-el {
  flex-grow: 3;
}
.second-el {
  padding: 0rem 5rem 10rem 5rem;
  flex-grow: 2;
}
</style>
