<template>
  <Home />
</template>

<script>
import Home from "./components/Home.vue";

export default {
  name: "Sprint-6",
  components: { Home },
  methods: {},
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;1,100;1,200;1,400;1,500&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
button {
  font-family: inherit;
  font-weight: 500;
}

#app {
  font-family: Poppins;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: teal;
}

</style>
