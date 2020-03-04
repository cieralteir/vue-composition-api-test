<template>
  <div>
    <button @click="increment">{{ count }}</button>
    <increment />
  </div>
</template>

<script lang="ts">
import { useIncrement } from "./compositions/use-increment";
import Increment from "./components/Increment.vue";

export default {
  components: {
    Increment
  },
  setup() {
    const { count, increment } = useIncrement();

    return {
      count,
      increment
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
