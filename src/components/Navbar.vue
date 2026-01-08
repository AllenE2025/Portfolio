<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const scrolled = ref(false)

const menuOpen = ref(false)

const navItems = [
    { name: 'Home', href: '#hero' },
    { name: 'About', href: '#about' },
    { name: 'Projects', href: '#projects' },
    { name: 'Contact', href: '#contact' },
]

const handleScroll = () => {
    scrolled.value = window.scrollY > 0
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll)

})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
})
</script>
<template>
    <nav :class="['fixed top-0 w-full z-50 text-white backdrop-blur transition-all duration-300',
        scrolled ? ' bg-black/40 shadow-lg' : 'bg-transparent'
    ]">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="text-2xl font-medium">Portfolio</div>

            <!-- Desktop Links -->
            <ul class="hidden md:flex space-x-6">
                <li v-for="item in navItems" :key="item.name">
                    <a :href="item.href"
                        class="inline-block text-xl font-medium transition-all hover:text-yellow-500 hover:scale-105 active:text-yellow-600 active:scale-95">
                        {{ item.name }}
                    </a>
                </li>
            </ul>

            <!-- Mobile Menu Button -->
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

        <!-- Mobile Links -->
        <div v-show="menuOpen" class="md:hidden">
            <ul class="flex flex-col space-y-2 px-4 py-2 bg-black/80">
                <li v-for="item in navItems" :key="item.name">
                    <a :href="item.href" @click="menuOpen = false" class="block text-white hover:text-yellow-500">
                        {{ item.name }}
                    </a>
                </li>
            </ul>
        </div>
    </nav>
</template>
