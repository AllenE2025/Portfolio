<script setup>
import techStack from '../data/techStack.json'
import { Icon } from '@iconify/vue'
</script>

<template>
  <div class="max-w-4xl mx-auto text-center md:text-left text-white place-items-center">


    <h2 class="text-5xl font-bold mb-4 bg-clip-text text-transparent 
             bg-linear-to-b from-white/60 via-yellow-400 to-yellow-600">
      About Me
    </h2>

    <div class="flex flex-col md:flex-row gap-10 p-5 rounded-md relative bg-neutral-900 overflow-hidden shadow-xl">

      <div class="pointer-events-none absolute top-0 left-0 right-0 h-0.75
                  bg-linear-to-b from-white/10 to-transparent"></div>
      <div class="absolute bottom-0 left-0 right-0 h-0.75 bg-linear-to-t from-black/30 to-transparent"></div>
      <div class="relative bg-neutral-800 overflow-hidden rounded-md p-4 mb-6 shadow-inner">
        <!-- Top gradient -->
        <div class="absolute top-0 left-0 right-0 h-1 bg-linear-to-t from-transparent to-black/60 pointer-events-none">
        </div>
        <!-- Bottom gradient -->
        <div
          class="absolute bottom-0 left-0 right-0 h-1 bg-linear-to-b from-transparent to-black/60 pointer-events-none">
        </div>
        <!-- Left gradient -->
        <div class="absolute top-0 bottom-0 left-0 w-1 bg-linear-to-l from-transparent to-black/60 pointer-events-none">
        </div>
        <!-- Right gradient -->
        <div
          class="absolute top-0 bottom-0 right-0 w-1 bg-linear-to-r from-transparent to-black/60 pointer-events-none">
        </div>
        <p class="text-lg text-gray-300 leading-relaxed tracking-wide">
          A Computer Engineering graduate from STI College Global City with a passion
          for building robust and efficient software solutions. I specialize in full-stack development using
          Vue.js, Laravel, and MySQL, and have hands-on experience with PHP, JavaScript, HTML, CSS, Node.js, and Python.

          I enjoy turning complex problems into intuitive, user-friendly applications. Having worked on multiple
          personal and collaborative projects, I constantly seek opportunities to learn, grow, and contribute to
          meaningful projects.

          In addition to coding, I focus on clean, maintainable code, collaborative teamwork, and leveraging
          modern frameworks and tools to deliver quality software.
        </p>

      </div>


      <img src="../assets/formal-fullbody.jpg" class="w-80 rounded-md mx-auto md:mx-0" />
    </div>
  </div>
</template>

