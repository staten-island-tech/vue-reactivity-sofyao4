<template>
  <div>
    <ul>
      <li v-for="grocery in groceries" :key="grocery.id">
        {{ grocery.name }} <firstButton>Add</firstButton>
      </li>
    </ul>
  </div>
</template>

<script>
import firstButton from "./first-button.vue";
export default {
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

<style lang="scss" scoped></style>
