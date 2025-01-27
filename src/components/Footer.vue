<template>
    <div class="flex flex-col">
        <main class="flex-grow"></main>

        <footer class="bg-[#383737] grid grid-cols-1 md:grid-cols-[30%_repeat(2,1fr)] gap-y-8 p-10 md:pr-32 pb-6">

            <div class="flex items-center">
                <a href="./" class="mt-0 mb-auto"><img :src="logo" alt="GO Platform Logo" class="h-[60px]"></a>
            </div>

            <div class="flex flex-col md:flex-row md:justify-between md:col-span-2 gap-12">
                <div class="text-white">
                    <h4 class="font-bold mb-4">About Us</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:underline">Company</a></li>
                        <li><a href="#" class="hover:underline">Contact Us</a></li>
                        <li><a href="#" class="hover:underline">Talents</a></li>
                    </ul>
                </div>

                <div class="text-white">
                    <h4 class="font-bold mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:underline">Blog</a></li>
                        <li><a href="#" class="hover:underline">Terms</a></li>
                        <li><a href="#" class="hover:underline">Privacy Policy</a></li>
                    </ul>
                </div>

                <div class="text-white">
                    <h4 class="font-bold mb-4">Socials</h4>
                    <ul class="space-y-2">
                        <li><a href="https://instagram.com/go.platform/" class="hover:underline">Instagram</a></li>
                        <li><a href="https://facebook.com/GO.Platform" class="hover:underline">Facebook</a></li>
                        <li><a href="https://linkedin.com/company/go-platform" class="hover:underline">LinkedIn</a></li>
                    </ul>
                </div>
            </div>


            <div class="text-center text-white md:col-span-3 mt-6">
                <p>&copy; {{year}} GO Platform.&nbsp;&nbsp;All rights reserved.</p>
            </div>
        </footer>
    </div>
</template>

<script setup>
import logo from '../assets/footer.png';
const year = new Date().getFullYear();
</script>