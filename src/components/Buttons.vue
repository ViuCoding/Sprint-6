<template>
  <div class="button-block">
    <button @click="$emit('changePhrase', 1)">Previous</button>
    <button @click="$emit('changePhrase', 2)">Next</button>
  </div>
</template>

<script>
export default {
  name: "Buttons",
};
</script>

<style>
.button-block {
  text-align: center;
}

.button-block button {
  padding: 1rem;
  border-radius: 30px;
  border: none;
  background-color: crimson;
  color: white;
  font-size: 1rem;
  cursor: crosshair;
  width: 20%;
  margin: 1rem;
}

.button-block button:active {
  transform: scale(0.96);
}
</style>
