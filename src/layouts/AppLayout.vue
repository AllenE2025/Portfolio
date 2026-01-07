<template>
    <div class="flex flex-col min-h-screen bg-black text-white">
        <!-- Navbar -->
        <Navbar />

        <!-- Main content -->
        <main class="flex-1">
            <slot />
        </main>

        <!-- Footer -->
        <footer class="text-center py-4 bg-black text-white">
            &copy; 2026 David Allen Evangelista. All rights reserved.
        </footer>
    </div>
</template>

<script setup>
import Navbar from '@/components/Navbar.vue'
</script>
