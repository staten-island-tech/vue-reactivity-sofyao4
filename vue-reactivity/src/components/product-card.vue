<template>
  <div>
    <ul>
      <li v-for="grocery in groceries" :key="grocery.name">
        {{ grocery.name }}
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
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-evenly;
}
li {
  margin-top: 2rem;

  margin: 4rem;
  padding: 3rem 9rem;

  width: 24%;
  border-radius: 2rem;
}
</style>
