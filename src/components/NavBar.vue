<template>
  <header>
    <section aria-label="App name">
      <h1>Portfolio</h1>
    </section>
    <section aria-label="Path section">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/projects">Projects</router-link>
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
    <button @click="toggleMenu" class="hamburger" aria-label="Toggle menu">
      ☰
    </button>
  </header>

  <div v-if="menuOpen" class="modal">
    <div class="modal-content">
      <button @click="toggleMenu" class="close" aria-label="Close menu">
        ✖
      </button>
      <nav>
        <router-link @click="toggleMenu" to="/">Home</router-link>
        <router-link @click="toggleMenu" to="/about">About</router-link>
        <router-link @click="toggleMenu" to="/projects">Projects</router-link>
        <a href="https://bsky.app/profile/xillians.bsky.social">
          <img src="../assets/socials/bluesky.png" alt="bsky" />
        </a>
        <a href="https://github.com/Xillians">
          <img
            src="../assets/socials/github-mark/github-mark.svg"
            alt="github"
          />
        </a>
        <a href="https://www.instagram.com/thexillyone/">
          <img src="../assets/socials/instagram.png" alt="instagram" />
        </a>
      </nav>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
const { menuOpen, toggleMenu } = useHamburgerMenu();

function useHamburgerMenu() {
  const menuOpen = ref(false);

  const toggleMenu = () => {
    menuOpen.value = !menuOpen.value;
  };

  return { menuOpen, toggleMenu };
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
img {
  width: 30px;
  height: 30px;
}

nav {
  display: flex;
  flex-direction: column;
  gap: 1em;
}

section[aria-label="Path section"],
section[aria-label="Social media links"] {
  display: flex;
  gap: 2em;
}

.hamburger {
  display: none;
  font-size: 2rem;
  background: none;
  border: none;
  cursor: pointer;
}

.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background: var(--lace);
  padding: 2rem;
  width: 25%;
  border-radius: 8px;
  text-align: center;
  button {
    font-size: 2rem;
    background: none;
    color: var(--sapphire);
    border: none;
    cursor: pointer;
  }
}

.close {
  position: absolute;
  top: 1rem;
  right: 1rem;
  font-size: 2rem;
  background: none;
  border: none;
  cursor: pointer;
}

@media (max-width: 768px) {
  .hamburger {
    display: block;
  }

  section[aria-label="Path section"],
  section[aria-label="Social media links"] {
    display: none;
  }
}
</style>
