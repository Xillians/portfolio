<template>
  <div class="LandingPage">
    <h1>{{ msg }}</h1>
    <p>
      Welcome to my portfolio! You can find me on the following locations<br />
      <a href="https://github.com/Xillians" target="_blank" rel="noopener"
        >github</a
      ><br />
      <a href="https://twitter.com/xillians" target="_blank" rel="noopener"
        >twitter</a
      ><br />
      <a href="https://www.twitch.tv/xillians" target="_blank" rel="noopener"
        >twitch</a
      ><br />
    </p>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
@Options({
  props: {
    msg: String
  }
})
export default class LandingPage extends Vue {
  msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
