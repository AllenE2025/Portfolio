<script setup>
import { Icon } from '@iconify/vue'
import projects from '../data/projects.json'
</script>

<template>
  <div class="max-w-4xl mx-auto px-6 md:px-0">
    <h2 class="text-5xl font-bold mb-8 text-center">Projects</h2>

    <div class="grid md:grid-cols-2 lg:grid-cols-2 gap-8">
      <div
        v-for="project in projects"
        :key="project.id"
        class="rounded-lg shadow-lg p-6 border border-yellow-500 flex flex-col justify-between"
      >
        <h3 class="text-xl font-medium mb-2">{{ project.title }}</h3>

        <p class="mb-4 text-justify flex-1">{{ project.description }}</p>

        <a
          :href="project.link"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-block w-34 text-center rounded-md p-2 font-semibold bg-yellow-500 text-black transition-all hover:scale-105 active:scale-95 active:bg-yellow-600 mb-4"
        >
          View Repository
        </a>

        <h3 class="text-lg font-medium mb-2">Technologies Used</h3>

        <div class="flex flex-wrap gap-6">
          <Icon
            v-for="tech in project.tech"
            :key="tech.name"
            :icon="tech.icon"
            class="w-12 h-12"
            :title="tech.name"
          />
        </div>
      </div>
    </div>
  </div>
</template>
