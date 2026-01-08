<script setup>
import { Icon } from '@iconify/vue'
</script>

<template>
    <div class="max-w-2xl mx-auto px-6 md:px-0 text-center">
        <h2
            class="text-5xl font-bold mb-6 bg-clip-text text-transparent bg-linear-to-b from-white/60 via-yellow-400 to-yellow-600">
            Contact Me</h2>

        <!-- Social Icons -->
        <div
            class="flex flex-col place-items-center justify-center gap-6 p-8 bg-neutral-900 rounded-lg relative overflow-hidden shadow-lg">
            <div class="relative bg-neutral-800 overflow-hidden rounded-md p-4 shadow-inner">
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

                <p class="text-lg text-gray-300 tracking-wide">
                    Reach out for collaborations or inquiries via my socials!
                </p>
            </div>
            <div class="flex"> <a href="https://www.linkedin.com/in/david-allen-evangelista-767878349/" target="_blank"
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

            <div class="pointer-events-none absolute top-0 left-0 right-0 h-0.75
        bg-linear-to-b
        from-white/10
        to-transparent
        ">
            </div>
            <div class="absolute bottom-0 left-0 right-0 h-0.75 bg-linear-to-t from-black/50 to-transparent
        "></div>
        </div>
    </div>
</template>
