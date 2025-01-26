<script setup>
import google from '../assets/google.png'
import ph from '../assets/ph.png'
import ratingImg from '../assets/Rating.png'

const ratings = [{
        name: 'Google',
        img: google,
        rating: 5.0,
        link: 'https://www.google.com'
    },
    {
        name: 'Product Hunt',
        img: ph,
        rating: 5.0,
        link: 'https://www.producthunt.com/products/go-platform'
    }
]


</script>
<template>
    <div class="mt-8 flex flex-wrap justify-around">
       <a v-for="rating in ratings" :href="rating.link" target="_blank"> <div class="bg-gray-100 w-[200px] h-[70px] rounded-full flex items-center justify-center cursor-pointer mt-4">
            <img :src="rating.img" alt="Google icon" class="h-10 " />
            <div class="ml-2">
                <p class="text-sm mb-1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{rating.name}}</p>
                <div class="flex"><p class="text-sm">5.0</p>&nbsp;
                    <img :src="ratingImg" alt="Ratings" class="w-24 h-4"></div>
            </div>
        </div></a>
    </div>
</template>