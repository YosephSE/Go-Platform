<template>
    <div :style="{ backgroundImage: `url(${back})` }">
    <NavBar />
    <section class="relative flex flex-wrap md:flex-nowrap md:pl-[100px] items-center py-16 px-8">
        <div class="w-3/4 md:w-1/2">

            <h1 class="text-4xl md:text-6xl font-bold justify-start">
                Discover the
            </h1>
            <h1 class="text-4xl md:text-6xl font-bold justify-start">
                potential
            </h1>
            <h1 class="text-4xl md:text-6xl font-bold mb-4 justify-start">
                of every talent
            </h1>
            <p class="text-md md:text-lg text-gray-700">
                Accurately measures competencies 
            </p>
            <p class="text-md md:text-lg text-gray-700 mb-6">
                and tracks skill progression
            </p>
            <button class="bg-yellow-500 text-white px-6 py-3 rounded-lg hover:bg-yellow-600">
                Start for free
            </button>
        </div>
        <div class="mt-16 md:mt-8">
            <img :src="heroImg" alt="Hero Image" class="w-170" />
        </div>
    </section>
    </div>
</template>

<script setup>
import heroImg from '../assets/hero.png'
import NavBar from './NavBar.vue'
import back from '../assets/i.png'
</script>