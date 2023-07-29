<script setup>
import football_1 from "/images/football_1.png";
import football_2 from "/images/football_2.png";
import football_3 from "/images/football_3.png";
import game_1 from "/images/game_1.png";
import game_2 from "/images/game_2.png";
import game_3 from "/images/game_3.png";
import ludo_1 from "/images/ludo_1.png";
import ludo_2 from "/images/ludo_2.png";
import ludo_3 from "/images/ludo_3.png";
import chess_1 from "/images/chess_1.png";
import chess_2 from "/images/chess_2.png";
import chess_3 from "/images/chess_3.png";
</script>

<template>
  <div class="player-section">
    <section id="football">
      <div class="main-card">
        <div class="label">微過返水 1.20 %</div>
        <img :src="football_1" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.20 %</div>
        <img :src="football_2" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.20 %</div>
        <img :src="football_3" alt="" />
      </div>
    </section>
    <section id="games">
      <div class="main-card">
        <div class="label">微過返水 1.25 %</div>
        <img :src="game_1" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.25 %</div>
        <img :src="game_2" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.25 %</div>
        <img :src="game_3" alt="" />
      </div>
    </section>
    <section id="ludo">
      <div class="main-card">
        <div class="label">微過返水 1.00 %</div>
        <img :src="ludo_1" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.00 %</div>
        <img :src="ludo_2" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.00 %</div>
        <img :src="ludo_3" alt="" />
      </div>
    </section>
    <section id="chess">
      <div class="main-card">
        <div class="label">微過返水 1.10 %</div>
        <img :src="chess_1" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.10 %</div>
        <img :src="chess_2" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.10 %</div>
        <img :src="chess_3" alt="" />
      </div>
    </section>
  </div>
</template>

<style scoped>
section,
.player-section {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.main-card {
  display: flex;
  flex-direction: column;
}
.label {
  background: linear-gradient(180deg, #feb68e, #f76f3f);
  width: fit-content;
  color: white;
  padding: 2px 20px;
  font-size: 12px;
  border-radius: 20px 0 30px 0;
  margin-bottom: -21px;
  z-index: 100;
}

img {
  width: 100%;
  height: 100%;
  max-width: 300px;
}
</style>
