<script setup lang="ts">
  import { ref } from "vue";

  import StickyFeedback from '../components/StickyFeedback.vue';
  import Header from '../components/Header.vue';
  import GridTiles from '../components/GridTiles.vue';
  import AboutPistons from "../components/AboutPistons.vue";
  import Testimonials from "../components/Testimonials.vue";
  import Footer from "../components/Footer.vue";

  const activeOverlay = ref(false);
</script>

<template>
  <div class="overlay"
    :class="{ active: activeOverlay }"
  />

  <StickyFeedback />
  <Header @toggleOverlay="activeOverlay = !activeOverlay" />

  <GridTiles />
  <AboutPistons />
  <Suspense>
    <Testimonials />
  </Suspense>
  <Footer />
</template>

<style>

@media screen and (max-width: 768px) {
  .overlay {
    width: 100%;
    position: absolute;
    height: 100vh;
    background-color: #000;
    opacity: 0.2;
    z-index: 1000000;
    display: none;
  }

  .overlay.active {
    display: block;
  }
}

</style>
