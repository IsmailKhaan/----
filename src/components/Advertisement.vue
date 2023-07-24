<script setup>
import { ref } from 'vue';
import promotion from '/images/promotion.png'

const isPromo = ref(true)
</script>

<template>
  <div v-if="isPromo" class="advertisement">
    <div @click="isPromo = !isPromo" class="cross"> &#9587</div>
    <img class="promo" :src="promotion" alt="">
    <div class="trife">立即下載</div>
  </div>
</template>

<style scoped>
.advertisement {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 16px;
  background-color: whitesmoke;
  position: sticky;
  top: 0;
}

.trife {
  border-radius: 20px;
  padding: 2px 8px;
  background-color: #F38245;
  color: white;
  font-size: 12px;
}
.promo{
  width: 280px;
  height: 60px;
  object-fit: cover;
}
.cross{
  font-size: 30px;
  color: #DEE3F1;
  font-weight:bolder;
}
</style>
