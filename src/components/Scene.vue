<template>
  <p v-for="phrase in history" :key="phrase">{{ phrase }}</p>
</template>

<script>
export default {
  name: "Scene",
  props: ["history"],
};
</script>

<style>
p {
  text-align: center;
  border: 2px solid black;
  padding: 1rem;
  border-radius: 30px;
}
</style>
   