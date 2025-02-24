<script setup lang="ts">
import { ref, computed } from "vue";
const { computedMessage } = useHome();

function useHome() {
  const message = ref("Hello Vue 3 + Vite");
  const computedMessage = computed(() => message.value + "!");
  return {
    message,
    computedMessage,
  };
}
</script>

<template>
  <div class="home">
    <h1>{{ computedMessage }}</h1>
  </div>
</template>
