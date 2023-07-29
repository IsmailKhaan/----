<script setup>
import SelectionMenu from "./SelectionMenu.vue";
import PlayersSection from "./PlayersSection.vue";
</script>

<template>
  <div class="view-player">
    <div class="menu">
      <SelectionMenu />
    </div>
    <div class="cards">
      <PlayersSection />
    </div>
  </div>
</template>

<style scoped>
.view-player {
  display: flex;
  justify-content: space-between;
  align-items: start;
  margin: 10px;
  margin-bottom: 100px;
  gap: 10px;
}
.cards {
  overflow-y: scroll;
}
</style>
