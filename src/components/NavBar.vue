<template>
    <header class="flex justify-between items-center py-4  px-[35px] md:px-[100px] bg-[#F8F8F8]/50 backdrop-blur-sm shadow-sm shadow-gray-300">
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
        <button class="hidden md:flex ml-auto md:ml-0 bg-sky-400 text-white px-6 py-2 rounded-lg">
            Log in
        </button>
        <div class="md:hidden">
            <img :src="menu" alt="Menu" class="h-6" />
        </div>
    </header>
</template>

<script setup>
import logo from '../assets/logo.svg'
import smlogo from '../assets/smlogo.png'
import menu from '../assets/menu.png'
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
  background: linear-gradient(to right, #ff0000, #00ffff);
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
</style>
