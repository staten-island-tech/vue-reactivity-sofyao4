<template>
  <div class="main">
    <div class="first-el">
      <productCard
        v-for="grocery in groceries"
        :key="grocery.name"
        :name="grocery.name"
        :price="grocery.price"
        :image="grocery.image"
      />
    </div>
    <div class="second-el">
      <h2>Your Cart</h2>
      <shopCart
        v-for="item in store.cart"
        :key="item.name"
        :name="item.name"
        :price="item.price"
      />
    </div>
  </div>
</template>

<script>
import productCard from "./product-card.vue";
import shopCart from "./shopCart.vue";
import { store } from "./store";

export default {
  name: "kuntainer",
  components: {
    productCard,
    shopCart,
  },
  data() {
    return {
      store,
      carts: [],
      groceries: [
        {
          name: "eggs",
          price: 9,
          image:
            "https://images.unsplash.com/photo-1536816579748-4ecb3f03d72a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80",
        },
        {
          name: "milk",
          price: 4,
          image:
            "https://images.unsplash.com/photo-1550583724-b2692b85b150?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80",
        },
        {
          name: "bread",
          price: 5,
          image:
            "https://images.unsplash.com/photo-1534620808146-d33bb39128b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80",
        },
        {
          name: "apples",
          price: 6,
          image:
            "https://images.unsplash.com/photo-1576179635662-9d1983e97e1e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80",
        },
        {
          name: "example 1",
          price: 6,
          image:
            "https://images.unsplash.com/photo-1542838132-92c53300491e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80",
        },
        {
          name: "example 2",
          price: 10,
          image:
            "https://images.unsplash.com/flagged/photo-1587302164675-820fe61bbd55?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80",
        },
      ],
    };
  },
};
</script>

<style scoped>
html,
body,
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  text-align: center;
}
h2 {
  text-align: center;
}
.main {
  display: flex;
}
.first-el {
  display: flex;
  flex-grow: 3;
  flex-direction: row;
  flex-wrap: wrap;
}
.second-el {
  padding: 1rem 6rem 0rem 5rem;
  flex-grow: 2;
}
</style>
