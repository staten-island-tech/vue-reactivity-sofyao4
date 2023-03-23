<template>
  <div>
    <ul>
      <li v-for="grocery in groceries" :key="grocery.name">
        <h2>
          {{ grocery.name }}
        </h2>
        <h3>Price: ${{ grocery.price }}</h3>

        <Button>Add</Button>
      </li>
    </ul>
  </div>
</template>

<script>
import Button from "./first-button.vue";
export default {
  components: {
    Button,
  },
  data() {
    return {
      groceries: [
        { name: "eggs", price: 9 },
        { name: "milk", price: 4 },
        { name: "bread", price: 5 },
        { name: "apples", price: 6 },
      ],
    };
  },
};
</script>

<style scoped>
ul {
  margin: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 100%;
}
li {
  background-color: aliceblue;

  list-style: none;
  margin: 2rem 2rem;
  padding: 3rem 5rem;

  border-radius: 2rem;
}
</style>
