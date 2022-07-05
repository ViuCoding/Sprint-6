<template>
  <Buttons />
  <Scene :history="history" />
</template>

<script>
import Buttons from "./Buttons.vue";
import Scene from "./Scene.vue";

export default {
  name: "Home",
  components: { Buttons, Scene },
  props: [],
  data() {
    return {
      history: ["Our hero was floating in outer space when in the distance he spotted a spaceship,", "He was curious about the interior of the ship and began to inspect it. He came to a room with two doors.", "The hero decided to go through the door that took him home,", "Meanwhile, other heroes weren't so lucky in their choice..."],
      currentSentence: 1,
    };
  },
};
</script>
