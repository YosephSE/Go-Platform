<script setup>
import google from '../assets/google.png'
import aws from '../assets/aws.svg'
import deloitte from '../assets/deloitte.png'
import EY from '../assets/EY.png'
import kpmg from '../assets/kpmg.png'
import pwc from '../assets/pwc.png'

const companies = [
    {name: 'Google', img: google},
    {name: 'AWS', img: aws},
    {name: 'EY', img: EY},
    {name: 'PWC', img: pwc},
    {name: 'KPMG', img: kpmg},
    {name: 'Deloitte', img: deloitte},
]
</script>

<template>
    <section class="bg-sky-50 py-10 md:py-16 inika-regular">
        <div class="container mx-auto px-4">
            <div class="flex justify-center items-center">
                <h1 class="text-xl md:text-2xl text-center mb-3 md:mb-6">
                    Our assessments are inspired by the <br>following companies
                </h1>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-8 md:gap-12 justify-items-center mt-8">
                <div v-for="company in companies" class="w-full flex justify-center items-center p-4 hover:cursor-pointer">
                    <img 
                        :src="company.img" 
                        :alt="company.name" 
                        class="h-16 md:h-20 w-auto object-contain"
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inika:wght@400;700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

.inika-regular {
  font-family: "Inika", serif;
  font-weight: 400;
  font-style: normal ;
}

.inika-bold {
  font-family: "Inika", serif;
  font-weight: 700;
  font-style: normal;
}</style>