<script setup>
import { reactive } from "vue";
import PlayerCard from "./PlayerCard.vue";
import player1 from "/images/player1.png";
import player2 from "/images/player2.png";
import xunli from "/images/xunli.png";
import saba from "/images/saba.png";

const players = reactive([
  {
    title: "微過返水 1.20 %",
    icon: xunli,
    name: "汛利体育",
    club: "XUNLI SPORTS",
    image: player1,
  },
  {
    title: "南高返水 1.18 %",
    icon: saba,
    name: "沙巴体育",
    club: "SABA SPORTS",
    image: player2,
  },
]);
</script>

<template>
  <div class="player-section">
    <div v-for="(player, index) in players" :key="index">
      <PlayerCard
        :title="player.title"
        :icon="player.icon"
        :name="player.name"
        :club="player.club"
        :image="player.image"
      />
    </div>
  </div>
</template>

<style>
.player-section {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>
