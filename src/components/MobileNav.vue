<template>
    <div :class="['absolute top-0 left-0 h-screen w-screen bg-black transform transition-transform duration-300 ease-in-out filter drop-shadow-md', open ? '-translate-y-0' : '-translate-y-full']">
      <div class="flex items-center justify-center filter drop-shadow-md bg-black h-20">
        <img src="/Tata_logo 1.png" class="w-auto h-auto">
      </div>
      <div class="flex flex-col items-center justify-center gap-y-6 py-10 text-lg text-black">
          <p class="text-white cursor-pointer transition-all duration-300" @click="setOpen(false)">Overview</p>
          <p class="hover:text-white cursor-pointer text-slate-300 transition-all duration-300" @click="setOpen(false)">Edition</p>
          <p class="hover:text-white cursor-pointer text-slate-300 transition-all duration-300" @click="setOpen(false)">Specs</p>
          <p class="hover:text-white cursor-pointer text-slate-300 transition-all duration-300" @click="setOpen(false)">Compare</p>
          <p class="hover:text-white cursor-pointer text-slate-300 transition-all duration-300" @click="setOpen(false)">Reviews</p>
          <p class="hover:text-white cursor-pointer text-slate-300 transition-all duration-300" @click="setOpen(false)">Price</p>
      </div>
    </div>
  </template>
  
  <script setup>  
  const props = defineProps({
    open: Boolean,
  });
  
  const emit = defineEmits(['set-open']);
  
  const setOpen = (val) => {
    emit('set-open', val);
  };
  </script>
  