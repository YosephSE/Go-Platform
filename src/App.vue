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
  <div>
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