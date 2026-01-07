<template>
    <div class="flex flex-col min-h-screen bg-[radial-gradient(circle,_#1C1C1C,_#0A0A0A)] text-white">
        <!-- Navbar -->
        <Navbar />

        <!-- Main content -->
        <main class="flex-1">
            <slot />
        </main>

        <!-- Footer -->
        <footer class="py-4 text-white flex justify-evenly">
            <!-- <div class="flex gap-2 place-items-center">
                <Icon icon="mingcute:phone-fill" /><span>+63 917-341-8437</span>
            </div> -->

            <span>&copy; 2026 David Allen Evangelista. All rights reserved.</span>
        </footer>
    </div>
</template>

<script setup>
import Navbar from '@/components/Navbar.vue'
// import { Icon } from '@iconify/vue'
</script>
