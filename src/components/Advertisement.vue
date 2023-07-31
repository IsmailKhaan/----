<script setup>
import { ref } from 'vue';

const isPromo = ref(true)
</script>

<template>
  <div v-if="isPromo" class="advertisement">
    <div @click="isPromo = !isPromo" class="cross"> &#9587</div>
    <div class="trife">立即下載</div>
  </div>
</template>

<style scoped>
.advertisement {
  transition: all ease-out .3s;
background: url('/images/promotion.png') no-repeat;
  background-size: 100% 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: whitesmoke;
  width: 957;
  overflow: hidden;
  height: 60px;
  padding: 0 14px;
}

.trife {
  border-radius: 14px;
  padding: 2px 11px;
  background: linear-gradient(180deg,#feb68e,#f76f3f);
  color: white;
  font-size: 12px;
}
.cross{
  font-size: 30px;
  color: #DEE3F1;
  font-weight:bolder;
}
</style>
