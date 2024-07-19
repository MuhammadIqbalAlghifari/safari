<template>
    <header ref="navbarRef" class="fixed z-50 w-full">
      <nav class="flex md:px-10 md:py-2 p-3 justify-between items-center w-full bg-[#121212] backdrop-blur-md bg-opacity-50 text-white">
        <MobileNav :open="open" @set-open="setOpen" />
        <img src="/Tata_logo 1.png" class="w-auto h-auto">
        <ul class="md:flex hidden items-center font-semibold justify-center lg:gap-x-14 gap-x-7 xl:text-xl text-lg">
          <li class="text-white transition-all duration-300 cursor-pointer">Overview</li>
          <li class="hover:text-white text-slate-300 transition-all duration-300 cursor-pointer">Edition</li>
          <li class="hover:text-white text-slate-300 transition-all duration-300 cursor-pointer">Specs</li>
          <li class="hover:text-white text-slate-300 transition-all duration-300 cursor-pointer">Compare</li>
          <li class="hover:text-white text-slate-300 transition-all duration-300 cursor-pointer">Reviews</li>
          <li class="hover:text-white text-slate-300 transition-all duration-300 cursor-pointer">Price</li>
        </ul>
        <div class="flex relative w-8 h-8 flex-col justify-between items-center md:hidden" @click="toggleOpen">
          <span :class="['h-1 w-full rounded-lg transform transition duration-300 ease-in-out', open ? 'rotate-45 translate-y-3.5 bg-white' : 'bg-white']"></span>
          <span :class="['h-1 w-full rounded-lg transform transition-all duration-300 ease-in-out', open ? 'w-0 h-0' : 'bg-white w-full']"></span>
          <span :class="['h-1 w-full rounded-lg transform transition duration-300 ease-in-out', open ? '-rotate-45 -translate-y-3.5 bg-white' : 'bg-white']"></span>
        </div>
      </nav>
    </header>
  </template>
  
  <script setup>
  import { ref, onMounted, onBeforeUnmount } from 'vue';
  import gsap from 'gsap';
  import MobileNav from './MobileNav.vue'; 
  
  const open = ref(false);
  const isScrolled = ref(false);
  const navbarRef = ref(null);
  
  const setOpen = (val) => {
    open.value = val;
  };
  
  const toggleOpen = () => {
    open.value = !open.value;
  };
  
  onMounted(() => {
    gsap.fromTo(navbarRef.value, { opacity: 0, y: -100 }, { opacity: 1, y: 0, duration: 1 });
  });
  
  onBeforeUnmount(() => {
  });
  </script>

  <style>
    .router-link-active {
      color: orange;
    }
  </style>
  