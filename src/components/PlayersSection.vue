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
import spot_1 from "/images/spot_1.png";
import spot_2 from "/images/spot_2.png";
import spot_3 from "/images/spot_3.png";
import pool_1 from "/images/pool_1.png";
import pool_2 from "/images/pool_2.png";
import pool_3 from "/images/pool_3.png";
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
    <section id="spot">
      <div class="main-card">
        <div class="label">微過返水 1.00 %</div>
        <img :src="spot_1" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.00 %</div>
        <img :src="spot_2" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 1.00 %</div>
        <img :src="spot_3" alt="" />
      </div>
    </section>
    <section id="pool">
      <div class="main-card">
        <div class="label">微過返水 0.00 %</div>
        <img :src="pool_1" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 0.00 %</div>
        <img :src="pool_2" alt="" />
      </div>
      <div class="main-card">
        <div class="label">微過返水 0.00 %</div>
        <img :src="pool_3" alt="" />
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
  /* background: linear-gradient(180deg, #feb68e, #f76f3f); */
  background: url("/images/bg_curved.png") no-repeat 50%;
  background-size: 100%;
  width: 121px;
  height: 30px;
  line-height: 23px;
  z-index: 10;
  text-align: center;
  font-size: 12px;
  color: #fff;
  font-size: 12px;
  margin-bottom: -30px;
}

img {
  width: 100%;
  height: 100%;
  max-width: 280px;
}
</style>
