<template>
    <div :style="{ backgroundImage: `url(${back})` }">
        <NavBar />
        <section class="relative flex flex-wrap md:flex-nowrap md:pl-[100px] items-center py-16 px-8">
            <div class="w-3/4 md:w-1/2">

                <h1 class="text-4xl md:text-6xl font-bold justify-start font-[poppins]">
                    Discover the
                </h1>
                <h1 class="text-4xl md:text-6xl font-bold justify-start font-[poppins]">
                    potential
                </h1>
                <h1 class="text-4xl md:text-6xl font-bold mb-4 md:mb-12 justify-start font-[poppins]">
                    of every talent
                </h1>
                <p class="md:hidden text-md md:text-lg text-gray-700">
                    Accurately measures competencies
                </p>
                <p class="md:hidden text-md md:text-lg text-gray-700 mb-6">
                    and tracks skill progression
                </p>
                <div class="flex"><button class="bg-[#EC9B04] text-black px-6 py-3 rounded-sm hover:bg-yellow-600 cursor-pointer">
                        Start for free
                    </button>
                    <div class="hidden md:block md:ml-4 m-0">
                        <p class="  md:text-xl text-gray-700 font-[Inika]">
                            Accurately measures competencies
                        </p>
                        <p class="md:text-xl text-gray-700 mb-6">
                            and tracks skill progression
                        </p>
                    </div>
                </div>


            </div>
            <div class="mt-16 md:mt-8">
                <img :src="heroImg" alt="Hero Image" class="w-170" />
                <Ratings />
            </div>
        </section>
    </div>
</template>

<script setup>
import heroImg from '../assets/hero.png'
import NavBar from './NavBar.vue'
import back from '../assets/i.png'
import Ratings from './Ratings.vue'
</script>
<style scoped></style>