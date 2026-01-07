<script setup>
import techStack from '../data/techStack.json'
import { Icon } from '@iconify/vue'
</script>

<template>
  <div class="max-w-4xl mx-auto text-center md:text-left text-white place-items-center">
    <!-- About Section -->
    <h2 class="text-5xl font-bold mb-4">About Me</h2>
    <div class="flex flex-col md:flex-row gap-10 p-5 rounded-md">
      <p class="text-lg text-justify">
        A Computer Engineering graduate from STI College Global City with a passion
        for building robust and efficient software solutions. I specialize in full-stack development using
        Vue.js, Laravel, and MySQL, and have hands-on experience with PHP, JavaScript, HTML, CSS, Node.js, and Python.

        I enjoy turning complex problems into intuitive, user-friendly applications. Having worked on multiple
        personal and collaborative projects, I constantly seek opportunities to learn, grow, and contribute to
        meaningful projects.

        In addition to coding, I focus on clean, maintainable code, collaborative teamwork, and leveraging
        modern frameworks and tools to deliver quality software.
      </p>
      <img src="../assets/formal-fullbody.jpg" class="w-80 rounded-md mx-auto md:mx-0" />
    </div>

    <!-- Tech Stack Section -->
    <section class="mt-12">
      <h2 class="text-4xl font-bold mb-6 text-center md:text-left">Tech Stack</h2>

      <!-- Scrollable carousel container -->
      <div class="overflow-x-auto flex gap-6 py-4 px-2 scrollbar-hide">
        <div
          v-for="tech in techStack"
          :key="tech.name"
          class="flex flex-col items-center min-w-[90px] shrink-0"
        >
          <Icon :icon="tech.icon" class="w-14 h-14 mb-2" :title="tech.name" />
          <span class="text-sm font-medium text-center">{{ tech.name }}</span>
        </div>
      </div>
    </section>
  </div>
</template>

<style>
/* Hide scrollbars nicely */
.scrollbar-hide::-webkit-scrollbar {
  display: none;
}

.scrollbar-hide {
  -ms-overflow-style: none;
  scrollbar-width: none;
}
</style>
