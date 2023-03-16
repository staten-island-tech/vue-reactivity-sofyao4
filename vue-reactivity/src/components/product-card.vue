<template>
  <div>
    <ul>
      <li v-for="grocery in groceries" :key="card.id>
      {{ grocery.name }}</li>
    </ul>
  </div>
</template>

<script>
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
