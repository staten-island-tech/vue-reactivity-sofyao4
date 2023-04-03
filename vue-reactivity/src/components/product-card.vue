<template>
  <div class="card">
    <h2>{{ name }}</h2>
    <img :src="image" alt="" />
    <h3>${{ price }}</h3>
    <Button @click="addTo">Add To Cart</Button>
  </div>
</template>

<script>
import Button from "./first-button.vue";
import { store } from "./store";
export default {
  name: "productCard",
  components: {
    Button,
  },
  props: {
    name: String,
    price: Number,
    image: String,
  },
  data() {
    return {
      store,
    };
  },
  methods: {
    addTo() {
      this.store.cart.push({
        name: this.name,
        price: this.price,
        image: this.image,
      });
    },
  },
};
</script>

<style scoped>
img {
  border-radius: 2rem;
  width: 10rem;
  max-height: 40rem;
}
.card {
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  text-align: center;
  background-color: #ca9a37;
  padding: 1rem;
  width: 20rem;
  border-radius: 5rem;
  font-weight: 600;
  margin: 3rem;
  transition: all 0.3s;
}
.card:hover {
  transform: translateY(-5px);
}
</style>
