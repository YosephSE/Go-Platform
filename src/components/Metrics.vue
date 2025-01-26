<script setup>
import { ref } from "vue";


const stats = ref([
  { title: "Turnover", value: "-73%" },
  { title: "Position Fit", value: "+98%" },
  { title: "Faster Skill growth", value: "8.25K" },
]);
</script>

<template>
  <section class="bg-gray-100 py-20 md:py-32 px-10">

    <div class="flex justify-center items-center mb-10">
      <h1 class="text-xl md:text-3xl text-center font-[poppins]">
        On average, enterprise employees that use GO PLATFORM see:
      </h1>
    </div>

    <div
      class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto my-20 md:my-28"
    >
      <div
        v-for="(box, index) in stats"
        :key="index"
        class="flex flex-col justify-center items-center p-8 bg-gradient-to-r from-[#09ADFF] to-[#0FEC8D] text-black rounded-2xl shadow-lg hover:scale-110 transition-transform duration-300 ease-in-out"
      >
        <h2 class="text-xl font-bold">{{ box.title }}</h2>
        <p class="text-4xl font-semibold">{{ box.value }}</p>
      </div>
    </div>
  </section>
</template>

<style>

</style>
