<script setup lang="ts">
import circus from "../assets/projects/circus.png";
import kingdom from "../assets/projects/kingdom.png";
import pathfinder from "../assets/projects/pathfinder.png";
import gapAnalyzer from "../assets/projects/gap-analyzer.png";
type Project = {
  name: string;
  description: string;
  // eslint-disable-next-line @typescript-eslint/no-explicit-any
  imageSrc: any;
  url: string;
  github?: string;
};

const projectList: Array<Project> = [
  {
    name: "Circus acts",
    description:
      "A website used during tabletop roleplaying games to track the progress and results of the show.",
    imageSrc: circus,
    url: "https://xillians.github.io/circus-acts/",
  },
  {
    name: "Kingdom Craft",
    description:
      "WiP: The adventure Kingmaker in pathfinder lets you control an expanding kingdom, and this tool helps you keep track of it.",
    imageSrc: kingdom,
    url: "https://xillians.github.io/kingdom-craft/",
  },
  {
    name: "Pathfinder Style",
    description:
      "For those that wish to use a standardised stylesheet for Pathfinder related applications, this project can help you out.",
    imageSrc: pathfinder,
    url: "https://xillians.github.io/pathfinder-style/",
  },
  {
    name: "Magic gap analyzer",
    description:
      "A helpful tool to identify what cards you are missing in your collection to complete your new Magic the Gathering deck.",
    imageSrc: gapAnalyzer,
    url: "https://xillians.github.io/what-am-i-missing/",
  },
];
</script>

<template>
  <h1>Projects</h1>
  <div class="project-card" v-for="project in projectList" :key="project.name">
    <div class="project-details">
      <a :href="project.url">
        <h2>{{ project.name }}</h2>
      </a>
      <p>{{ project.description }}</p>
    </div>
    <img :src="project.imageSrc" alt="Circus acts" />
  </div>
</template>

<style scoped>
.project-card {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  text-align: left;
  padding: 0.5rem;
}
h2 {
  margin: 0;
}

.project-details {
  display: flex;
  flex-direction: column;
  width: 100%;
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
