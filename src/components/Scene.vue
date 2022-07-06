<template>
  <p v-for="(phrase, index) in story" :key="index" :class="{ active: index === sentence }">{{ phrase }}</p>
</template>

<script>
export default {
  name: "Scene",
  props: ["story", "sentence"],
};
</script>

<style scoped>
p {
  text-align: center;
  border: 2px solid teal;
  padding: 1rem;
  border-radius: 30px;
}

.active {
  background-color: #00ff01;
  color: steelblue;
}
</style>
