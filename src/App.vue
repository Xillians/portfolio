<template>
  <header-vue />
  <main-body title="Welcome to my portfolio!" />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import headerVue from "./components/header.vue";
import MainBody from "./components/mainBody.vue";

@Options({
  components: {
    headerVue,
    MainBody,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
