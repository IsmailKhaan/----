<script setup>
import SelectionMenu from "./SelectionMenu.vue";
import PlayersSection from "./PlayersSection.vue";
</script>

<template>
  <div class="view-player">
    <SelectionMenu />
    <PlayersSection />
  </div>
</template>

<style>
.view-player {
  display: flex;
  align-items: start;
  gap: 10px;
  padding: 8px;
}
</style>
