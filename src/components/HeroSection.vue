<template>
    <div :style="{ backgroundImage: `url(${back})` }">
        <section class="relative flex flex-wrap md:flex-nowrap md:pl-[100px] items-center py-32 px-8 inika-bold">
            <div class="w-3/4 md:w-1/2">

                <h1 class="text-4xl md:text-6xl font-bold justify-start">
                    Discover the
                </h1>
                <h1 class="text-4xl md:text-6xl font-bold justify-start">
                    potential
                </h1>
                <h1 class="text-4xl md:text-6xl font-bold mb-4 md:mb-12 justify-start">
                    of every talent
                </h1>
                <p class="md:hidden text-md md:text-lg text-gray-700">
                    Accurately measures competencies
                </p>
                <p class="md:hidden text-md md:text-lg text-gray-700 mb-6">
                    and tracks skill progression
                </p>
                <div class="flex"><button class="bg-yellow-500 text-black px-6 py-3 rounded-sm hover:bg-yellow-600 cursor-pointer hover:scale-110 transition">
                        Start for free
                    </button>
                    <div class="hidden md:block md:ml-4 m-0">
                        <p class="  md:text-xl text-gray-700 font-[Inika]">
                            Accurately measures competencies
                        </p>
                        <p class="md:text-xl text-gray-700 mb-6">
                            and tracks skill progression
                        </p>
                    </div>
                </div>


            </div>
            <div class="mt-16 md:mt-8">
                <img :src="heroImg" alt="Hero Image" class="w-170" />
                <Ratings />
            </div>
        </section>
    </div>
</template>

<script setup>
import heroImg from '../assets/hero.png'
import back from '../assets/i.png'
import Ratings from './Ratings.vue'
</script>
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

.text-box {
    margin-left: 44vw;
    margin-top: 42vh;
}

.btn:link,
.btn:visited {
    text-transform: uppercase;
    text-decoration: none;
    padding: 15px 40px;
    display: inline-block;
    border-radius: 100px;
    transition: all .2s;
    position: absolute;
}

.btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.btn:active {
    transform: translateY(-1px);
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}

.btn-white {
    background-color: #fff;
    color: #777;
}

.btn::after {
    content: "";
    display: inline-block;
    height: 100%;
    width: 100%;
    border-radius: 100px;
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1;
    transition: all .4s;
}

.btn-white::after {
    background-color: #fff;
}

.btn:hover::after {
    transform: scaleX(1.4) scaleY(1.6);
    opacity: 0;
}

.btn-animated {
    animation: moveInBottom 5s ease-out;
    animation-fill-mode: backwards;
}

@keyframes moveInBottom {
    0% {
        opacity: 0;
        transform: translateY(30px);
    }

    100% {
        opacity: 1;
        transform: translateY(0px);
    }
}</style>