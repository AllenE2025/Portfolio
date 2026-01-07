<template>
  <AppLayout>
    <section id="hero" class="min-h-screen flex items-center justify-center ">
      <Hero />
    </section>

    <section id="about" class="min-h-screen flex items-center justify-center ">
      <About />
    </section>

    <section id="projects" class="min-h-screen flex items-center justify-center ">
      <Projects />
    </section>

    <section id="contact" class="min-h-screen flex items-center justify-center ">
      <Contact />
    </section>
  </AppLayout>
</template>

<script setup>
import AppLayout from './layouts/AppLayout.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
</script>

<style>
html {
  scroll-behavior: smooth;
}
</style>
