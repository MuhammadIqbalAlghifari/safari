<script setup>
import { onMounted } from 'vue';
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue';
import Picture from './components/Picture.vue';
import Lenis from 'lenis';

onMounted(() => {
  const lenis = new Lenis()

  function raf(time) {
    lenis.raf(time)
    requestAnimationFrame(raf)
  }

  requestAnimationFrame(raf)
});
</script>

<template>
  <Navbar/>
  <Hero/>
  <Picture/>
</template>
