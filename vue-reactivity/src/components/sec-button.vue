<template>
  <div>
    <button><slot></slot></button>
  </div>
</template>

<script>
export default {
  name: "remove",
  props: {
    name: String,
    price: Number,
  },
};
</script>

<style scoped>
button {
  background-color: #874f38;
}
</style>
