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
        <div class="flex justify-center items-center">
            <h1 class="text-xl md:text-3xl text-center font-[poppins]">
                Our assessment are inspired by the <br>following companies
            </h1>
        </div>
        <div class="flex flex-wrap justify-center items-center mt-8">
            <img v-for="company in companies" :src="company.img" :alt="company.name" class="h-20 mt-12 mx-10 md:mx-10" />

        </div>
    </section>
</template>