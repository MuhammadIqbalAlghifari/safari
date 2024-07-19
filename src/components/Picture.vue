<template>
    <div class="w-full h-full flex flex-col justify-center px-5 gap-y-5 lg:py-40 py-20 items-center">
        <h1 ref="tittleOneRef" class="xl:text-3xl md:text-2xl text-xl font-extrabold text-white" style="font-family: 'Sora Variable';">The Grand Design</h1>
        <p ref="tittleTwoRef" class="text-slate-300 xl:text-xl md:text-lg text-base text-center max-w-lg" style="font-family: 'SF Regular';">The new safari showcases an artistic sensibility that’s sophisticated, assertive and way ahead of its time</p>
        <main ref="imageCarRef" class="flex-col lg:py-20 py-10 flex max-w-4xl w-full h-auto justify-center items-center gap-y-2">
            <div class="w-full h-full relative overflow-hidden flex justify-end items-end">
                <img src="/grille crop.jpg" class="md:w-auto w-full brightness-50 h-auto object-cover object-center">
                <div class="h-full absolute z-20 flex flex-col items-start p-2 justify-end">
                    <h1 class="lg:text-lg text-sm md:text-base font-bold text-white" style="font-family: 'Sora Variable';">New Parametric Grille</h1>
                    <h1 class="lg:text-sm text-xs text-white max-w-xs" style="font-family: 'SF Regular';">First impressions should always leave an indelible mark. The New Safari’s Parametric Grille is designed to do just that. It makes the frontal stance bolder and masculine, captivating the onlooker instantly.</h1>
                </div>
            </div>
            <div class="flex flex-col md:flex-row justify-center md:gap-x-2 md:gap-y-0 gap-y-2 w-full h-full items-center">
                <div class="w-auto h-full relative overflow-hidden flex justify-start items-end">
                    <img src="/oyster-white-interior-theme.jpg" class="md:w-auto w-full brightness-50 h-auto object-cover object-center">
                    <div class="h-full absolute z-20 flex flex-col items-start md:p-10 p-4 justify-end">
                        <h1 class="lg:text-lg text-sm md:text-base font-bold text-white" style="font-family: 'Sora Variable';">New Parametric Grille</h1>
                        <h1 class="lg:text-sm text-xs text-white max-w-xs" style="font-family: 'SF Regular';">First impressions should always leave an indelible mark. The New Safari’s Parametric Grille is designed to do just that. It makes the frontal stance bolder and masculine, captivating the onlooker instantly.</h1>
                    </div>
                </div>
                <div class="w-auto h-auto relative overflow-hidden flex justify-end items-end">
                    <img src="/garasi.png" class="md:w-auto w-full brightness-50 h-auto object-cover object-center">
                    <div class="h-full absolute z-20 flex flex-col items-start p-2 justify-start">
                        <h1 class="lg:text-lg text-sm md:text-base font-bold text-white" style="font-family: 'Sora Variable';">New Parametric Grille</h1>
                        <h1 class="lg:text-sm text-xs text-white max-w-xs" style="font-family: 'SF Regular';">First impressions should always leave an indelible mark. The New Safari’s Parametric Grille is designed to do just that. It makes the frontal stance bolder and masculine, captivating the onlooker instantly.</h1>
                    </div>
                </div>
            </div>
            <div class="flex flex-col-reverse md:flex-row justify-center md:gap-x-2 md:gap-y-0 gap-y-2 w-full h-full items-center">
                <div class="w-auto h-full relative overflow-hidden flex justify-start items-end">
                    <img src="/safari back.jpg" class="md:w-auto w-full brightness-50 h-auto object-cover object-center">
                    <div class="h-full absolute z-20 flex flex-col items-start p-4 justify-end">
                        <h1 class="lg:text-lg text-sm md:text-base font-bold text-white" style="font-family: 'Sora Variable';">New Parametric Grille</h1>
                        <h1 class="lg:text-sm text-xs text-white max-w-xs" style="font-family: 'SF Regular';">First impressions should always leave an indelible mark. The New Safari’s Parametric Grille is designed to do just that. It makes the frontal stance bolder and masculine, captivating the onlooker instantly.</h1>
                    </div>
                </div>
                <div class="w-auto h-full relative overflow-hidden flex justify-start items-end">
                    <img src="/steer.jpg" class="md:w-auto w-full brightness-50 h-auto object-cover object-center">
                    <div class="h-full absolute z-20 flex flex-col items-start p-4 justify-end">
                        <h1 class="lg:text-lg text-sm md:text-base font-bold text-white" style="font-family: 'Sora Variable';">New Parametric Grille</h1>
                        <h1 class="lg:text-sm text-xs text-white max-w-xs" style="font-family: 'SF Regular';">First impressions should always leave an indelible mark. The New Safari’s Parametric Grille is designed to do just that. It makes the frontal stance bolder and masculine, captivating the onlooker instantly.</h1>
                    </div>
                </div>
            </div>
        </main>
        <h1 ref="tittleThreeRef" class="xl:text-3xl md:text-2xl text-xl font-extrabold text-white" style="font-family: 'Sora Variable';">The All New Design</h1>
        <button ref="buttonRef" class="px-6 py-3 border-white flex justify-center items-center gap-x-5 border">
            <p class="xl:text-2xl md:text-xl text-lg text-white text-center max-w-lg" style="font-family: 'SF Medium';">Find Dealer Now</p>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="size-6 p-1 rounded-full bg-white text-black">
                <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5 21 12m0 0-7.5 7.5M21 12H3" />
            </svg>
        </button>    
    </div>
</template>
<script setup>
import gsap from 'gsap';
import ScrollTrigger from 'gsap/dist/ScrollTrigger';
import { onMounted, ref } from 'vue';

const tittleOneRef = ref(null)
const tittleTwoRef = ref(null)
const tittleThreeRef = ref(null)
const buttonRef = ref(null)
const imageCarRef = ref(null)

onMounted(() => {
    gsap.registerPlugin(ScrollTrigger)
    gsap.fromTo(tittleOneRef.value, {opacity: 0, y: 50}, {opacity: 1, y: 0, duration: 1, ease: 'power3.out', scrollTrigger: {
        trigger: tittleOneRef.value,
        start: 'top bottom',
        end: 'center center',
        scrub: true
    }})
    gsap.fromTo(tittleTwoRef.value, {opacity: 0, y: 50}, {opacity: 1, y: 0, duration: 1, ease: 'power3.out', scrollTrigger: {
        trigger: tittleTwoRef.value,
        start: 'top bottom',
        end: 'center center',
        scrub: true
    }})
    gsap.fromTo(tittleThreeRef.value, {opacity: 0, y: 50}, {opacity: 1, y: 0, duration: 1, ease: 'power3.out', scrollTrigger: {
        trigger: tittleThreeRef.value,
        start: 'top bottom',
        end: 'center center',
        scrub: true
    }})
    gsap.fromTo(buttonRef.value, {opacity: 0, y: 50}, {opacity: 1, y: 0, duration: 1, ease: 'power3.out', scrollTrigger: {
        trigger: buttonRef.value,
        start: 'top bottom',
        end: 'center center',
        scrub: true
    }})
    imageCarRef.value.childNodes.forEach(child => {
        gsap.fromTo(child, {opacity: 0, y: 50}, {opacity: 1, y: 0, duration: 1, ease: 'power3.out', scrollTrigger: {
            trigger: child,
            start: 'top bottom',
            end: 'center center',
            scrub: true
        }})
    })
})

</script>