<template>
  <div v-if="showSplash" id="splash">
    <h1>Welcome to Planet Monchi 141</h1>
    <p>
      This is the story of Subject 41. His quest was like none other. <br />
      A new video game he really liked just came out so he just HAD to get home and play it. <br />
      This is how it went down...
    </p>
    <button @click="toggleCanvass">START YOUR JOURNEY</button>
  </div>
  <div v-if="showCanvass">
    <Buttons @changePhrase="changePhrase" />
    <Scene :story="story" :sentence="currentSentence" />
  </div>
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
      showSplash: true,
      showCanvass: false,
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

    toggleCanvass() {
      this.showCanvass = !this.showCanvass;
      this.showSplash = !this.showSplash;
    },
  },
};
</script>

<style>
#splash {
  background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.6)), url("../assets/img/bg1.jpg") center/cover;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
}
#splash h1 {
  color: crimson;
  text-transform: uppercase;
  font-weight: 600;
  text-shadow: 6px 4px 1px white;
  font-size: 5rem;
}
#splash p {
  font-size: 1.7rem;
  margin: 2rem 0;
  color: white;
  text-shadow: 1px 1px 1px crimson;
}

#splash button {
  font-size: 1.6rem;
  padding: 1.5rem;
  border-radius: 11px;
  border: none;
  cursor: crosshair;
  background-color: crimson;
  color: white;
}

#splash button:active {
  transform: scale(0.96);
}
</style>
