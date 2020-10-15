<template>
  <img alt="Vue logo" src="./assets/logo.png" class="logo" /><br />
  <div class="note">
    <a>Profile picture is drawn by DevicatOutlet. <br /></a>
    <a>You can find her on </a>
    <a href="https://www.twitch.tv/devicat" target="_blank" rel="noopener"
      >twitch</a
    >
    <a> or </a>
    <a href="https://twitter.com/DeviCatOutlet" target="_blank" rel="noopener"
      >twitter
    </a>
  </div>
  <HelloWorld msg="Xillians portfolio" />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import HelloWorld from "./components/HelloWorld.vue";

@Options({
  components: {
    HelloWorld
  }
})
export default class App extends Vue {}
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

.logo {
  align-content: center;
  height: 250 px;
  width: 250px;
}

.note {
  font-family: Avenit, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: darkslategrey;
  font-size: 12px;
}
</style>
