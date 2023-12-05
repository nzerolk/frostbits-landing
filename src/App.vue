<template>
  <div id="app">
    <Hero/>
    <Features/>
    <Team/>
    <Footer/>
  </div>
</template>

<script>
import {defineComponent} from "vue";
import Hero from "./components/Hero.vue";
import Features from "./components/Features.vue";
import Team from "./components/Team.vue";
import Footer from "./components/Footer.vue";

export default defineComponent({
  components: {Footer, Team, Hero, Features}
})
</script>

<style scoped>
</style>
