<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    name: String,
    price: Number,
  },
};
</script>

<style scoped>
button {
  font-size: 15px;
  color: #f3f2f1;
  background-color: #874f38;
}
</style>
