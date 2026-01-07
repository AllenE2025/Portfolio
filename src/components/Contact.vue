<script setup>
import { Icon } from '@iconify/vue'
</script>

<template>
    <div class="max-w-2xl mx-auto px-6 md:px-0 text-center">
        <h2 class="text-5xl font-bold mb-6">Contact Me</h2>
        <p class="text-lg mb-6">Reach out for collaborations or inquiries via my socials!</p>

        <!-- Social Icons -->
        <div class="flex justify-center gap-6">
            <a href="https://www.linkedin.com/in/david-allen-evangelista-767878349/" target="_blank"
                rel="noopener noreferrer">
                <Icon icon="mdi:linkedin"
                    class="w-24 h-24 transition-all hover:scale-105 hover:text-yellow-500 active:scale-95 active:text-yellow-600" />
            </a>

            <a href="https://github.com/AllenE2025" target="_blank" rel="noopener noreferrer">
                <Icon icon="mdi:github"
                    class="w-24 h-24 transition-all hover:scale-105 hover:text-yellow-500 active:scale-95 active:text-yellow-600" />
            </a>

            <a href="mailto:evangelista.davidallen2003@gmail.com">
                <Icon icon="mdi:gmail"
                    class="w-24 h-24 transition-all hover:scale-105 hover:text-yellow-500 active:scale-95 active:text-yellow-600" />
            </a>
        </div>
    </div>
</template>
