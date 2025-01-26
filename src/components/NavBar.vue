<template>
    <header
        class=" fixed top-0 left-0 w-full  z-50 flex justify-between items-center py-4 px-[35px] md:px-[100px] bg-[#F8F8F8]/50 backdrop-blur-sm shadow-sm shadow-gray-300"
    >

        <div class="hidden md:flex items-center space-x-2">
            <a href="/"><img :src="logo" alt="Logo" class="h-10" /></a>
        </div>


        <div class="flex md:hidden items-center space-x-2">
            <a href="/"><img :src="smlogo" alt="Logo" class="h-10" /></a>
        </div>

        <nav class="hidden md:flex space-x-8 text-lg">
            <a href="#" class="hover-underline">Product</a>
            <a href="#" class="hover-underline">Pricing</a>
            <a href="#" class="hover-underline">Resources</a>
        </nav>
        <button class="hidden md:flex ml-auto md:ml-0 bg-sky-400 text-white px-6 py-2 rounded-lg cursor-pointer">
            Log in
        </button>

        <div class="md:hidden relative">
            <img :src="menu" alt="Menu" class="h-6" @click="showMenu = !showMenu" />
        </div>
    </header>

    <transition name="slide-down">
        <div
            v-if="showMenu"
            class="fixed inset-0 bg-white z-50 flex flex-col p-4 space-y-4 text-lg"
        >
            <div class="flex justify-end">
                <img
                    :src="menu"
                    alt="Close"
                    class="h-6"
                    @click="showMenu = false"
                />
            </div>
            <a href="#" class="block hover-underline">Product</a>
            <a href="#" class="block hover-underline">Pricing</a>
            <a href="#" class="block hover-underline">Resources</a>
            <button class="bg-sky-400 text-white px-6 py-2 rounded-lg w-full cursor-pointer">
                Log in
            </button>
        </div>
    </transition>
</template>

<script setup>
import { ref } from 'vue'
import logo from '../assets/logo.svg'
import smlogo from '../assets/image.png'
import menu from '../assets/menu.png'

const showMenu = ref(false)
</script>

<style scoped>
.hover-underline {
    position: relative;
    display: inline-block;
}
.hover-underline::after,
.hover-underline::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 2px;
    background: linear-gradient(to right, #000, #000);
    bottom: -5px;
    left: 0;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 0.4s ease-out;
}
.hover-underline::before {
    top: -5px;
    transform-origin: left;
}
.hover-underline:hover::after,
.hover-underline:hover::before {
    transform: scaleX(1);
}

.slide-down-enter-active,
.slide-down-leave-active {
    transition: transform 0.3s ease;
}
.slide-down-enter {
    transform: translateY(-100%);
}
.slide-down-leave-to {
    transform: translateY(-100%);
}
</style>
