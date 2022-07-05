<template>
  <div class="button-block">
    <button @click="test">Previous</button>
    <button @click="test">Next</button>
  </div>
</template>

<script>
export default {
  name: "Buttons",

  methods: {
    test() {
      console.log("CLICK");
    },
  },
};
</script>

<style>
.button-block {
  text-align: center;
}

.button-block button {
  padding: 1.5rem;
  border-radius: 30px;
  border: none;
  background-color: crimson;
  color: white;
  font-size: 1rem;
  cursor: crosshair;
  width: 40%;
  margin: 1rem;
}
</style>
