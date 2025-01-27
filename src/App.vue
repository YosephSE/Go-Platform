<script setup>
import NavBar from './components/NavBar.vue';
import AboutUs from './components/AboutUs.vue';
import HeroSection from './components/HeroSection.vue'
import Metrics from './components/Metrics.vue';
import Partners from './components/Partners.vue'
import Services from './components/services.vue';
import Testimony from './components/Testimony.vue';
import Footer from './components/Footer.vue';

</script>

<template>
  <div class="inika-regular">
    <NavBar />
    <HeroSection />
    <Partners />
    <Testimony />
    <Metrics />
    <Services />
    <AboutUs />
    <Footer />
  </div>
</template>


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
}
</style>