<template>
    <div class="pb-24 bg-sky-50">
        <h1 class="text-xl md:font-bold md:text-2xl text-center pt-16 md:pb-0 px-12 pb-16"> Assessments to reveal workforce readiness beyond resumes!</h1>

        <div class="grid grid-cols-1 md:grid-cols-[60%_40%] items-center justify-center gap-8 px-8 md:p-16">
            <div class="md:pl-8">
                <div class="">
                    <div class="h-[45px] w-[150px] bg-gray-300 rounded-full flex items-center justify-center">
                        <img :src="robot" alt="Robot image" class="h-[30px] pr-2" />
                        <span>Automation</span>
                    </div>
                    <p class="font-bold pt-7 pl-2 text-xl"><span class="text-sky-400">Save time</span> with <span
                            class="text-sky-400">automated</span> that drive actions</p>
                    <ul class="list-disc pl-8 pt-4 text-lg">
                        <li>Accelerate your recruitment cycle with automated workflows.</li>
                        <li>Reduce the manual work and improve time-to-hire.</li>
                        <li>Create a positive and seamless experience for job applicants.</li>
                        <li>Manage all candidates in one platform, improving organization and data accessibility.</li>
                        <li>Make informed decisions based on real-time recruitment analytics and reports.</li>
                    </ul>
                </div>
            </div>
            <div class="mt-4">
                <img :src="about" alt="About us image" class="h-96 w-96" />
            </div>
        </div>
    </div>

</template>

<script setup>
import about from '../assets/about.png'
import robot from '../assets/robot.png'
</script>

<style>
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
}</style>