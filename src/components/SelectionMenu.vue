<script setup>
import { reactive, ref } from "vue";
import football from "/images/football.png";
import games from "/images/games.png";
import persons from "/images/persons.png";
import chess from "/images/chess.png";

const buttons = reactive([
  {
    icon: football,
    text: "体育",
    to: "/#football",
  },
  {
    icon: games,
    text: "电竞",
    to: "/#games",
  },
  {
    icon: persons,
    text: "真人",
    to: "/#ludo",
  },
  {
    icon: chess,
    text: "棋牌",
    to: "/#chess",
  },
]);
const activeIndex = ref(0);
</script>

<template>
  <div class="player-menu">
    <div
      class="btn"
      v-for="(btn, index) in buttons"
      :key="index"
      @click="activeIndex = index"
    >
      <a
        class="btn-content"
        :class="index === activeIndex ? 'active' : ''"
        :href="btn.to"
      >
        <img :src="btn.icon" alt="icon" />
        <div>{{ btn.text }}</div>
      </a>
    </div>
  </div>
</template>

<style scoped>
.player-menu {
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-size: 14px;
  gap: 6px;
  /* position: fixed; */
}
.btn {
  padding: 4px;
  background-color: white;
  border-radius: 14px;
}

.btn-content {
  padding: 6px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 4px;
  color: gray;
  text-decoration: none;
  border-radius: 14px;
  align-items: center;
  background-color: white;
  border: none;
}

.active {
  background: linear-gradient(180deg, #feb68e, #f76f3f);
  color: white;
  outline: none;
}
img {
  width: 40px;
}
</style>
