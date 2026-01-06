<template>
    <nav class="fixed top-0 w-full bg-white shadow z-50">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="text-xl font-bold">David Allen</div>

            <!-- Desktop links -->
            <ul class="hidden md:flex space-x-6">
                <li><a href="#hero">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

            <!-- Mobile menu button -->
            <button @click="menuOpen = !menuOpen" class="md:hidden focus:outline-none">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path v-if="!menuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M4 8h16M4 16h16" />
                    <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M6 18L18 6M6 6l12 12" />
                </svg>
            </button>
        </div>

        <!-- Mobile links -->
        <div v-show="menuOpen" class="md:hidden">
            <ul class="flex flex-col space-y-2 px-4 py-2">
                <li><a href="#hero" @click="menuOpen = false">Home</a></li>
                <li><a href="#about" @click="menuOpen = false">About</a></li>
                <li><a href="#projects" @click="menuOpen = false">Projects</a></li>
                <li><a href="#contact" @click="menuOpen = false">Contact</a></li>
            </ul>
        </div>
    </nav>
</template>

<script setup>
import { ref } from 'vue'
const menuOpen = ref(false)
</script>
