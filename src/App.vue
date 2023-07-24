<script setup>
import HeroSection from "./components/HeroSection.vue";
import ViewPlayers from "./components/ViewPlayers.vue";
import Advertisement from "./components/Advertisement.vue";
import Navigations from "./components/Navigations.vue";
</script>

<template>
  <Advertisement />
  <div class="main">
    <HeroSection />
    <ViewPlayers />
  </div>
  <Navigations />
</template>

<style>
body {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  background-color: #ebeefd;
  display: flex;
  justify-content: center;
  font-family: sans-serif;
  color: gray;
}

.main {
  overflow-y: scroll;
}
</style>
