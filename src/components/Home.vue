<template>
  <Buttons @changePhrase="changePhrase" />
  <Scene :story="story" :sentence="currentSentence" />
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
      story: ["Our hero was floating in outer space when in the distance he spotted a spaceship,", "He was curious about the interior of the ship and began to inspect it. He came to a room with two doors.", "The hero decided to go through the door that took him home,", "Meanwhile, other heroes weren't so lucky in their choice..."],
      currentSentence: 0,
    };
  },
  methods: {
    changePhrase(id) {
      if (id === 1) {
        this.currentSentence--;
      } else {
        this.currentSentence++;
      }

      if (this.currentSentence < 0) this.currentSentence = 3;
      if (this.currentSentence > 3) this.currentSentence = 0;
    },
  },
};
</script>
