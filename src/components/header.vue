<template>
  <nav id="navbar" class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <a id="navbar title" class="navbar-brand" href="#">Portfolio</a>
      <div class="navbar-collapse" id="">
        <ul class="navbar-nav me-auto">
          <li class="nav-item" v-for="link in nav_links" :key="link.title">
            <a class="nav-link" :href="link.href">{{ link.title }}</a>
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
  data() {
    return {
      nav_links: [
        {
          href: "#",
          title: "Home",
        },
        {
          href: "https://www.instagram.com/thexillyone/",
          title: "instagram",
        },
        {
          href: "https://twitter.com/xillians",
          title: "Twitter",
        },
      ],
    };
  },
})
export default class HeaderVue extends Vue {
  nav_links: any;
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
