<script setup>
import { ref } from "vue";


const stats = ref([
  { title: "Turnover", value: "-73%" },
  { title: "Position Fit", value: "+98%" },
  { title: "Faster Skill growth", value: "8.25K" },
]);
</script>

<template>
  <section class="bg-sky-100 py-20 md:py-32 px-10">

    <div class="flex justify-center items-center mb-10">
      <h1 class="text-xl md:text-3xl text-center inika-regular">
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

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inika:wght@400;700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

.inika-regular {
  font-family: "Inika", serif;
  font-weight: 400;
  font-style: normal;
}

.inika-bold {
  font-family: "Inika", serif;
  font-weight: 700;
  font-style: normal;
}

</style>
