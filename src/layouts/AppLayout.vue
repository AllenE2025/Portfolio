<template>
    <div class="flex flex-col min-h-screen">
        <!-- Navbar -->
        <Navbar />

        <!-- Main content -->
        <main class="flex-1">
            <slot />
        </main>

        <!-- Footer -->
        <footer class="text-center py-4">
            &copy; 2026 David Allen Evangelista. All rights reserved.
        </footer>
    </div>
</template>

<script setup>
import Navbar from '@/components/Navbar.vue'
</script>
