<template>
  <button @click="increment">{{ count }}</button>
</template>

<script lang="ts">
import { useIncrement } from "../compositions/use-increment";

export default {
  setup() {
    const { count, increment } = useIncrement();

    return {
      count,
      increment
    };
  }
};
</script>
