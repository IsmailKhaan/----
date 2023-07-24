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
  },
  {
    icon: games,
    text: "电竞",
  },
  {
    icon: persons,
    text: "真人",
  },
  {
    icon: chess,
    text: "棋牌",
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
      <button
        class="btn-content"
        :class="index === activeIndex ? 'active' : ''"
      >
        <img :src="btn.icon" alt="icon" />
        <div>{{ btn.text }}</div>
      </button>
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
  border-radius: 14px;
  align-items: center;
  background-color: white;
  border: none;
}

.active {
  background-color: #f38245;
  color: white;
  outline: none;
}
img {
  width: 40px;
}
</style>
