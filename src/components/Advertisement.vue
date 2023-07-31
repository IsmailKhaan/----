<script setup>
import { ref } from 'vue';
import promotion from '/images/promotion.png'
const isPromo = ref(true)
</script>

<template>
  <div v-if="isPromo" class="advertisement">
    <div @click="isPromo = !isPromo" class="cross"> &#9587</div>
    <img class="promo" :src="promotion" alt="promo">
    <div class="trife">立即下載</div>
  </div>
</template>

<style scoped>
.advertisement {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: whitesmoke;
  height: 60px;
  padding: 0 14px;
  overflow: hidden;
}

.trife {
  border-radius: 14px;
  padding: 2px 11px;
  background: linear-gradient(180deg,#feb68e,#f76f3f);
  color: white;
  font-size: 12px;
}
img{
  width: 60%;
  height: 70px;
  object-fit: fill;
}
.cross{
  font-size: 20px;
  color: #DEE3F1;
  font-weight:bolder;
}
</style>
