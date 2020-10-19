<template>
  <div class="Gallery">
    <h2>{{title}}</h2>
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
    title: String
  }
})
export default class Gallery extends Vue {
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
