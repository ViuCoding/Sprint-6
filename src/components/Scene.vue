<template>
  <p v-for="phrase in history" :key="phrase">{{ phrase }}</p>
</template>

<script>
export default {
  name: "Scene",
  props: ["history", "sentence"],
};
</script>

<style scoped>
p {
  text-align: center;
  border: 2px solid black;
  padding: 1rem;
  border-radius: 30px;
}

.active {
  background: turquoise;
  color: black;
}
</style>
