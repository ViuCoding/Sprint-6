<template>
  <p v-for="(phrase, index) in story" :key="index" :class="{ active: index === sentence }">{{ phrase.txt }}</p>
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
  background-color: rgba(255, 255, 255, 0.6);
  color: crimson;
  padding: 0.8rem;
  font-weight: 600;
  border-radius: 30px;
  margin: 0px 10rem 1rem 10rem;
}

.active {
  background-color: rgba(255, 255, 255, 1);
  outline: solid 3px crimson;
}
</style>
