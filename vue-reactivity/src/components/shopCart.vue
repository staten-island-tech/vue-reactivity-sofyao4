<template>
  <div>
    <div v-show="itemsInCart" class="items">
      <h2>{{ name }}</h2>
      <h3>${{ price }}</h3>
      <remove @click="itemsInCart = !itemsInCart"> X </remove>
    </div>
  </div>
</template>

<script>
import remove from "./sec-button.vue";

export default {
  name: "shopCart",
  props: {
    name: String,
    price: Number,
  },
  components: {
    remove,
  },
  data() {
    return {
      total: 1,
      itemsInCart: true,
    };
  },
  methods: {},
};
</script>

<style scoped></style>
