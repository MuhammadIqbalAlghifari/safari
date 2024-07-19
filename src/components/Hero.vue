<template>
    <div class="overflow-hidden">
        <div ref="parallaxRef"class="w-full h-screen relative">
            <section ref="heroRef" class="h-full absolute z-0 flex justify-start items-center md:px-10 px-5 w-full">
                <div class="flex-col flex lg:gap-y-10 gap-y-5 justify-center max-w-3xl lg:items-start items-center">
                    <h1 class="text-white font-bold xl:text-8xl lg:text-7xl md:text-6xl text-4xl" style="font-family: 'Sora Variable';">The New Safari</h1>
                    <p class="text-slate-200 xl:text-2xl md:text-xl text-lg max-w-2xl text-center lg:text-start" style="font-family: 'SF Regular';">The New Safari carries on the legendary lineage with contemporary and premium updates. The New Safari is a compelling combination of Grand Design, Cutting-edge Technology & Luxurious Comfort</p>
                    <button class="flex md:px-6 md:py-3 px-4 py-2 border-white border justify-start items-center gap-x-5">
                        <p class="text-white xl:text-2xl md:text-xl text-lg" style="font-family: 'Sf Medium';">Book Now</p>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="md:size-6 size-6 p-1 rounded-full bg-white">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5 21 12m0 0-7.5 7.5M21 12H3" />
                        </svg>
                    </button>
                </div>
            </section>
            <img src="/hero.jpg" class="absolute -z-20 w-full h-full object-cover object-right brightness-90">
            <div class="absolute h-full -z-10 w-full bg-gradient-to-r from-black to-transparent opacity-50"></div>
            <h1 ref="scaleRef" class="uppercase 2xl:scale-[500] lg:scale-[300] scale-[400] lg:text-[172.32px] sm:text-9xl text-7xl font-extrabold mix-blend-multiply text-white bg-black absolute w-full h-full z-10 flex justify-center items-center" style="font-family: 'Urbanist Variable';">safari</h1>
            <div ref="scrollRef" class="flex opacity-0 absolute z-20 justify-center w-full h-full items-end py-20">
                <button class="flex justify-center text-white items-center gap-x-5">
                    <p class="uppercase xl:text-2xl md:text-xl text-lg tracking-widest">scroll down</p>
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="size-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 17.25 12 21m0 0-3.75-3.75M12 21V3" />
                    </svg>
                </button>
            </div>
        </div>
    </div>
</template>
<script setup>
import gsap from 'gsap';
import ScrollTrigger from 'gsap/dist/ScrollTrigger';
import { onMounted, ref } from 'vue';

const parallaxRef = ref(null)
const heroRef = ref(null)
const scaleRef = ref(null)
const scrollRef = ref(null)

onMounted(() => {
        gsap.registerPlugin(ScrollTrigger)
        const tl = gsap.timeline({
            defaults: {duration: 0.5}, 
            scrollTrigger: {
                trigger: parallaxRef.value,
                start: 'top top',
                end: '3000 bottom',
                scrub: true,
                pin: true
            }
        });
        tl.to(heroRef.value, { y: '+=1000' }, 0);
        tl.to(scaleRef.value, { scale: 1 }, 0.1);
        tl.to(scrollRef.value, { opacity: 1}, 0.6);
});

</script>