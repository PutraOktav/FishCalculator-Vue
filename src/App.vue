<!-- src/App.vue -->
<template>
  <div id="app">
    <FishCalculator />
  </div>
</template>

<script>
import FishCalculator from "./components/FishCalculator.vue";

export default {
  name: "App",
  components: {
    FishCalculator,
  },
};
</script>

<style>
#app {
  font-family: "Arial", sans-serif;
  text-align: center;
  background-color: #f0f0f0;
  padding: 2rem;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
