<script setup>
import { Icon } from '@iconify/vue';
import projects from '../data/projects.json';
import techStack from '../data/techStack.json'

</script>

<template>
  <div class="w-full mx-auto px-6 md:px-0">
    <!-- Section Title -->
    <h2
      class="text-5xl font-bold mb-8 bg-clip-text text-transparent bg-linear-to-b from-white/60 via-yellow-400 to-yellow-600 text-center">
      Projects
    </h2>

    <!-- Horizontal row of cards -->
    <div class="flex flex-wrap justify-center gap-8 items-stretch">
      <div v-for="project in projects" :key="project.id"
        class="w-105 rounded-xl p-6 bg-neutral-900 shadow-lg 
               relative overflow-hidden flex flex-col justify-between transition-all duration-300 hover:-translate-y-2 hover:shadow-xl">

        <!-- Top edge highlight -->
        <div class="pointer-events-none absolute top-0 left-0 right-0 h-1 bg-linear-to-b from-white/10 to-transparent">
        </div>

        <!-- Project Title -->
        <h3 class="text-xl font-medium mb-2 text-gray-200 relative">
          {{ project.title }}
        </h3>

        <!-- Description with inset/concave effect -->
        <div class="flex-1 relative bg-neutral-800 overflow-hidden rounded-md p-4 mb-4 shadow-inner">
          <!-- Top gradient -->
          <div
            class="absolute top-0 left-0 right-0 h-1 bg-linear-to-t from-transparent to-black/60 pointer-events-none">
          </div>
          <!-- Bottom gradient -->
          <div
            class="absolute bottom-0 left-0 right-0 h-1 bg-linear-to-b from-transparent to-black/60 pointer-events-none">
          </div>
          <!-- Left gradient -->
          <div
            class="absolute top-0 bottom-0 left-0 w-1 bg-linear-to-l from-transparent to-black/60 pointer-events-none">
          </div>
          <!-- Right gradient -->
          <div
            class="absolute top-0 bottom-0 right-0 w-1 bg-linear-to-r from-transparent to-black/60 pointer-events-none">
          </div>

          <p class="leading-relaxed tracking-wide text-gray-300 relative">
            {{ project.description }}
          </p>
        </div>

        <!-- Repository Link -->
        <a :href="project.link" target="_blank" rel="noopener noreferrer"
          class="inline-block w-34 text-center rounded-md p-2 font-semibold bg-yellow-500 text-black transition-all hover:scale-105 active:scale-95 active:bg-yellow-600 relative overflow-hidden mb-4">
          View Repository
          <div
            class="pointer-events-none absolute bg-linear-to-t from-yellow-900 to-transparent bottom-0 left-0 right-0 h-0.75">
          </div>
        </a>

        <!-- Technologies -->
        <h3 class="text-lg font-medium mb-2 text-gray-200 relative">
          Technologies Used
        </h3>
<div class="flex gap-2">
          <div v-for="tech in project.tech" :key="tech.name" :icon="tech.icon" :title="tech.name"
            class="relative bg-neutral-800 overflow-hidden rounded-md p-2 shadow-inner flex justify-center text-gray-300 w-auto">
            <!-- Top gradient -->
            <div
              class="absolute top-0 left-0 right-0 h-1 bg-linear-to-t from-transparent to-black/60 pointer-events-none">
            </div>
            <!-- Bottom gradient -->
            <div
              class="absolute bottom-0 left-0 right-0 h-1 bg-linear-to-b from-transparent to-black/60 pointer-events-none">
            </div>
            <!-- Left gradient -->
            <div
              class="absolute top-0 bottom-0 left-0 w-1 bg-linear-to-l from-transparent to-black/60 pointer-events-none">
            </div>
            <!-- Right gradient -->
            <div
              class="absolute top-0 bottom-0 right-0 w-1 bg-linear-to-r from-transparent to-black/60 pointer-events-none">
            </div>

            {{ tech.name }}

          </div>
        </div>
       
      </div>
    </div>

    <!-- <section class="mt-12">
      <h2 class="text-4xl font-bold mb-6 bg-clip-text text-transparent 
           bg-linear-to-b from-white/60 via-yellow-400 to-yellow-600 text-center">
        Tech Stack
      </h2>


      <div class="max-w-4xl mx-auto relative overflow-hidden rounded-xl py-4 px-5">

        <div class="flex gap-6 animate-scroll whitespace-nowrap">

          <div v-for="tech in [...techStack, ...techStack]" :key="tech.name + Math.random()" class="inline-flex flex-col items-center min-w-22 shrink-0 rounded-md 
                  bg-neutral-900 p-4 shadow-lg transition-transform duration-300 
                  hover:-translate-y-2 hover:shadow-xl text-gray-200 relative overflow-hidden">


            <div class="pointer-events-none absolute top-0 left-0 right-0 h-0.75
                    bg-linear-to-b from-white/10 to-transparent"></div>

            <Icon :icon="tech.icon" class="w-18 h-18 mb-2" :title="tech.name" />
            <span class="text-sm font-medium text-center text-gray-300">{{ tech.name }}</span>
          </div>
        </div>


        <div class="pointer-events-none absolute top-0 left-0 bottom-0 w-16 
                bg-linear-to-r from-neutral-900 to-transparent"></div>

        <div class="pointer-events-none absolute top-0 right-0 bottom-0 w-16 
                bg-linear-to-l from-neutral-900 to-transparent"></div>
      </div>
    </section> -->
  </div>
</template>

<style>
.scrollbar-hide::-webkit-scrollbar {
  display: none;
}

.scrollbar-hide {
  -ms-overflow-style: none;
  scrollbar-width: none;
}


@keyframes scroll {
  0% {
    transform: translateX(0);
  }

  100% {
    transform: translateX(-50%);
  }
}

.animate-scroll {
  animation: scroll 20s linear infinite;
}

/* Optional: pause on hover */
.animate-scroll:hover {
  animation-play-state: paused;
}
</style>