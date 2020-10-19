<template>
  <div class="helloWorld">
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
  <div class="Gallery">
    <ul>
      <li v-for="item in gallery" :key="item.name">
        <img class="thumbnail" :src="item.img" :alt="item.name" /><br />
        <a :href="item.href" target="_blank" rel="noopener">{{item.name}}</a>
      </li>
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
export class Gallery extends Vue {
  data() {
    return {
      gallery: [
        {
          img: "https://i.imgur.com/SGfSfme.jpg",
          href: "https://imgur.com/a/LSnhoHN",
          name: "daedric dagger"
        },
        {
          img: "https://i.imgur.com/XX5xWgb.jpg",
          href: "https://imgur.com/a/PCLLwz6",
          name: "chain chomp"
        },
        {
          img: "https://i.imgur.com/ylVck7d.jpg",
          href: "https://imgur.com/a/EyxGB4d",
          name: "samus aran"
        }
      ]
    };
  }
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
  border-radius: 50px;
  width: 500px;
  height: 300px;
}
</style>
