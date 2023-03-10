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
  color: pink;
  font-size: 15px;
}
</style>
