<template>
  <Home :history="history" />
</template>

<script>
import Home from "./components/Home.vue";

export default {
  name: "Sprint-6",
  components: { Home },
  data() {
    return {
      history: ["Our hero was floating in outer space when in the distance he spotted a spaceship,", "He was curious about the interior of the ship and began to inspect it. He came to a room with two doors.", "The hero decided to go through the door that took him home,", "Meanwhile, other heroes weren't so lucky in their choice..."],
    };
  },

  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: teal;
}
</style>
