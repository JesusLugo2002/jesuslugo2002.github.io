<script setup lang="ts">
import About from './components/About.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import MySkills from './components/MySkills.vue';
import MyWorks from './components/MyWorks.vue';
</script>

<template>
  <Header>Jesús Lugo</Header>
  <main>
    <Hero/>
    <About/>
    <MySkills/>
    <MyWorks/>
    <Contact/>
  </main>
  <Footer>© Jesús Lugo 2025</Footer>
</template>

<style lang="scss">
body {
  background-color: $white;
}
</style>