<script setup lang="ts">
import circus from "../assets/projects/circus.png";
import { ref } from "vue";
const { circusImage } = useImages();
type Project = {
  name: string;
  description: string;
  url: string;
};

const projectList: Array<Project> = [
  {
    name: "Circus acts",
    description:
      "A website used during tabletop roleplaying games to track the progress and results of the show.",
    url: "https://xillians.github.io/circus-acts/",
  },
  {
    name: "Kingdom Craft",
    description:
      "WiP: The adventure Kingmaker in pathfinder lets you control an expanding kingdom, and this tool helps you keep track of it.",
    url: "https://xillians.github.io/kingdom-craft/",
  },
  {
    name: "Pathfinder Style",
    description:
      "For those that wish to use a standardised stylesheet for Pathfinder related applications, this project can help you out.",
    url: "https://xillians.github.io/pathfinder-style/",
  },
  {
    name: "Magic gap analyzer",
    description:
      "A helpful tool to identify what cards you are missing in your collection to complete your new Magic the Gathering deck.",
    url: "https://xillians.github.io/magic-gap-analyzer/",
  },
];
function useImages() {
  const circusImage = ref(circus);
  return {
    circusImage,
  };
}
</script>

<template>
  <h1>Projects</h1>
  <div class="project-card" v-for="project in projectList" :key="project.name">
    <a :href="project.url">
      <h2>{{ project.name }}</h2>
    </a>
    <div class="project-details">
      <p>{{ project.description }}</p>
      <img :src="circusImage" alt="Circus acts" />
    </div>
  </div>
</template>

<style scoped>
.project-card {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  text-align: left;
  padding: 1rem;
  margin: 1rem;
}

.project-details {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

img {
  width: 250px;
  height: auto;
}
@media (max-width: 768px) {
  img {
    width: 135px;
    height: 100%;
  }
}
</style>
