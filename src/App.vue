<script setup>
import Navbar from "./components/NavBar.vue";
</script>

<template>
  <Navbar />
  <router-view />
</template>

<style src="./stylesheet.css"></style>

<style>
#app {
  font-family: var(--font-family);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--text-color);
}
</style>
