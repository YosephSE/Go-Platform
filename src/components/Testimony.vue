<script setup>
import tback from '../assets/tback.png'
import t1 from '../assets/t1.png'
import t2 from '../assets/t2.png'
import t3 from '../assets/t3.png'
import { ref } from 'vue'

const testimonials = ref([
    {
        id: 1,
        name: 'Fernando Lucini',
        image: t1,
        testimony: 'GO Platform has created a consistent and unbiased way to measure our workforce, providing unparalleled insights into employee performance, aligning with our strategic goals, and empowering us to make data-driven decisions like never before.',
    },
    {
        id: 2,
        name: 'Jane Smith',
        image: t2,
        testimony: 'The platform has been a game changer for our team collaboration, enabling deeper connections, fostering an environment of trust and transparency, and significantly enhancing the way we work together toward shared objectives.',
    },
    {
        id: 3,
        name: 'Michael Brown',
        image: t3,
        testimony: 'Its seamless integration has improved our productivity exponentially, reducing operational inefficiencies, streamlining complex workflows, and allowing us to focus on driving meaningful outcomes for our organization.',
    },
])


const currentIndex = ref(0)

const showNext = () => {
    currentIndex.value = (currentIndex.value + 1) % testimonials.value.length
}

const showPrev = () => {
    currentIndex.value =
        (currentIndex.value - 1 + testimonials.value.length) % testimonials.value.length
}
</script>

<template>
    <section class="min-h-[75vh] flex items-center justify-center" :style="{ backgroundImage: `url(${tback})` }">
        <div class="relative flex items-center">

            <button class="absolute left-0 -translate-x-1/2 bg-white rounded-full p-3 shadow-lg hover:shadow-xl"
                @click="showPrev">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-600" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
                </svg>
            </button>

            <transition name="fade">
                <div class="flex justify-center items-center w-full">
                    <div v-if="testimonials[currentIndex]" :key="testimonials[currentIndex].id"
                        class="bg-white shadow-lg rounded-lg p-6 text-center max-w-md transition-all duration-500 min-h-[50vh] flex items-center justify-center">
                        <div>
                            <div class="w-20 h-20 mx-auto rounded-full overflow-hidden border-2 border-gray-300">
                                <img :src="testimonials[currentIndex].image" :alt="testimonials[currentIndex].name" />
                            </div>
                            <h3 class="mt-4 text-xl font-semibold">{{ testimonials[currentIndex].name }}</h3>
                            <p class="mt-2 text-gray-600 px-8">
                                "{{ testimonials[currentIndex].testimony }}"
                            </p>
                        </div>
                    </div>
                </div>
            </transition>

            <button class="absolute right-0 translate-x-1/2 bg-white rounded-full p-3 shadow-lg hover:shadow-xl"
                @click="showNext">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-600" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                </svg>
            </button>
        </div>
    </section>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.5s;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
</style>
