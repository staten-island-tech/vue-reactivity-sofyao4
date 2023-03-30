<template>
  <div class="main">
    <div class="first-el">
      <productCard></productCard>
    </div>
    <div class="second-el"></div>
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

<style lang="scss">
.main {
  display: flex;
}
.first-el {
  display: flex;
  flex-grow: 7;
}
.second-el {
  flex-grow: 3;
}
</style>
