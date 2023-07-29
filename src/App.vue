<script setup>
import Advertisement from "./components/Advertisement.vue";
import HeroSection from "./components/HeroSection.vue";
import ViewPlayers from "./components/ViewPlayers.vue";
import Navigations from "./components/Navigations.vue";
</script>

<template>
  <div class="main">
    <Advertisement />
    <HeroSection />
  </div>
  <ViewPlayers />
  <Navigations />
</template>

<style>
body {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  background-color: #ebeefd;
  font-family: Helvetica, Arial, sans-serif;
  color: #6d7ba8;
  overflow-x: hidden;
}
.main {
  position: sticky;
  top: 0;
  z-index: 200;
}
.swiper-pagination-bullet {
  width: 10px;
  height: 10px;
  background-color: white;
  opacity: 1;
}
.swiper-pagination-bullet-active {
  background-color: #ff7700 !important;
}
</style>
