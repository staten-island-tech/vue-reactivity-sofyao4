<script setup>
import mainHeader from "./components/rootcomp.vue";
import shopCart from "./components/shopCart.vue";
import kuntainer from "./components/flex-container.vue";
</script>

<template>
  <div>
    <mainHeader></mainHeader>
  </div>
  <kuntainer></kuntainer>
</template>

<style scoped>
body,
* {
  margin: 8% 4%;
  padding: 0;
  box-sizing: border-box;

  text-align: center;
}
</style>
