<template>
  <div class="helloWorld">
    <h1>{{ msg }}</h1>
    <p>
      Welcome to my portfolio! You can find me on the following locations<br>
      <a 
        href="https://github.com/Xillians" 
        target="_blank" 
        rel="noopener"
        >github</a
      ><br>
      <a 
        href="https://twitter.com/xillians" 
        target="_blank" 
        rel="noopener"
        >twitter</a
      ><br>
      <a 
        href="https://www.twitch.tv/xillians" 
        target="_blank" 
        rel="noopener"
        >twitch</a
      ><br>
    </p>
    <h3>imgur gallery</h3>
    <ul>
      <img class="thumbnail" src="https://i.imgur.com/SGfSfme.jpg" alt="dagger"><br>
      <a
        href="https://imgur.com/a/LSnhoHN"
        target="_blank"
        rel="noopener"
        >daedric dagger</a
      >
    </ul>
    <ul>
      <img class="thumbnail" src="https://i.imgur.com/XX5xWgb.jpg" alt="dagger"><br>
      <a
        href="https://imgur.com/a/PCLLwz6"
        target="_blank"
        rel="noopener"
        >chain chomp</a
      >
    </ul>
    <ul>
      <img class="thumbnail" src="https://i.imgur.com/ylVck7d.jpg" alt="dagger"><br>
      <a
        href="https://imgur.com/a/EyxGB4d"
        target="_blank"
        rel="noopener"
        >samus aran</a
      >
    </ul>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    msg: String
  }
})
export default class HelloWorld extends Vue {
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
.thumbnail {
  width: 500px;
  height: 300px;
}
</style>
