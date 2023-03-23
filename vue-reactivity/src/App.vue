<script setup>
import productCard from "./components/product-card.vue";
import mainHeader from "./components/rootcomp.vue";
import shopCart from "./components/shopCart.vue";
</script>

<template>
  <div>
    <mainHeader></mainHeader>
    <productCard />
  </div>
</template>

<style scoped>
body,
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-size: 62.5%;
  text-align: center;
}
</style>
