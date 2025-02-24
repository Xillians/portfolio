<template>
  <header>
    <section aria-label="App name">
      <h1>Portfolio</h1>
    </section>
    <section aria-label="Path section">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/projects">Projects</router-link>
      <router-link to="/socials">socials</router-link>
    </section>
    <section aria-label="Social media links" style="justify-self: end">
      <a href="https://bsky.app/profile/xillians.bsky.social">
        <img src="../assets/socials/bluesky.png" alt="bsky" />
      </a>

      <a href="https://github.com/Xillians">
        <img src="../assets/socials/github-mark/github-mark.svg" alt="github" />
      </a>

      <a href="https://www.instagram.com/thexillyone/">
        <img src="../assets/socials/instagram.png" alt="instagram" />
      </a>
    </section>
  </header>
</template>

<style scoped>
header {
  display: grid;
  grid-template-columns: 0.4fr 3fr 0.5fr;
  align-items: center;
}

section {
  display: flex;
  flex-direction: row;
  gap: 2em;
}
img {
  cursor: pointer;
  height: 25px;
}
</style>
