<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "Button",
};
</script>

<style scoped>
button {
  color: gray;
  font-size: 15px;
  background-color: azure;
}
</style>
