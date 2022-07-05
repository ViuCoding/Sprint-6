<template>
  <p v-for="phrase in history" :key="phrase">{{ phrase }}</p>
</template>

<script>
export default {
  name: "Scene",
  props: ["history"],
};
</script>
