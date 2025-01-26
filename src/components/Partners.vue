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
    <section class="bg-[#F7F7F7] py-10 md:py-16">
        <div class="container mx-auto px-4">
            <div class="flex justify-center items-center">
                <h1 class="text-xl md:text-3xl text-center font-[poppins]">
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