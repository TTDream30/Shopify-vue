<template>
  <button>{{ text }}</button>
</template>
<script>
export default {
  name: "Button",
  props: {
    text: String,
  },
};
</script>
<style scoped>
button {
  padding: 10px;
  font-weight: bold;
  color: white;
  background: #c03553;
  border-radius: 12px;
  border: 0;
}
</style>