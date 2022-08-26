<template>
  <nav id="navbar" class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <a id="navbar title" class="navbar-brand" href="#">Portfolio</a>
      <div class="navbar-collapse" id="">
        <ul class="navbar-nav me-auto">
          <li class="nav-item">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://www.instagram.com/thexillyone/"
              >Instagram</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://twitter.com/xillians">Twitter</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  name: "header",
  props: {
    msg: String,
  },
})
export default class HelloWorld extends Vue {
  msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
