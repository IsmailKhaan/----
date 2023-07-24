<script setup>
import { reactive } from "vue";
import Payments from "./Payments.vue";
import cover from "/images/cover.png";
import deposite from "/images/deposite.png";
import transfer from "/images/transfer.png";
import withdraw from "/images/withdraw.png";
import vip from "/images/vip.png";
import speak from "/images/speak.png";
import xunli from "/images/xunli.png";
import sound from "/images/sound.png";

const paymentMethods = reactive([
  {
    icon: deposite,
    text: "存款",
  },
  {
    icon: transfer,
    text: "转账",
  },
  {
    icon: withdraw,
    text: "取款",
  },
  {
    icon: vip,
    text: "贵宾",
  },
]);
</script>

<template>
  <div class="hero-section">
    <div class="header">
      <div class="header-left">
        <img class="club-icon" :src="xunli" alt="icon" />
        <div>
          <div class="heading">汛利娱乐</div>
          <div class="link">www.xunli.bet</div>
        </div>
      </div>
      <img class="header-right" :src="speak" alt="icon" />
    </div>
    <img class="carousel" :src="cover" alt="cover" />
    <div class="input">
      <div class="sound-icon">
        <img :src="sound" alt="icon" />
      </div>
      <input type="text" placeholder="XXXXXXXXXXXXXXXXXXXXXXXXXXX" />
      <div class="submit">更多</div>
    </div>
    <div class="footer">
      <div class="footer-left">
        <div class="footer-top">您还未登录</div>
        <div class="footer-bottom">登录/注册后查看</div>
      </div>
      <div class="footer-right">
        <div v-for="(payment, index) in paymentMethods" :key="index">
          <Payments :icon="payment.icon" :text="payment.text" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-section {
  display: flex;
  flex-direction: column;
  gap: 10px;
  background-color: white;
  padding: 10px;
  border-radius: 0 0 20px 20px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px,
    rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}
.sound-icon {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 100%;
  height: 20px;
  width: 20px;
  padding: 1px;
  background-color: #f38245;
}
.header-left {
  display: flex;
  align-items: center;
  gap: 4px;
}

.header-right {
  width: 20px;
}

.carousel {
  height: 200px;
  width: 400px;
  border-radius: 16px;
  margin-left: -24px;
}

.input {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 4px;
  background-color: #f1f2f8;
  border-radius: 20px;
}

input {
  flex: 1;
  background: transparent;
  outline: none;
  border: none;
}

.footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.footer-top {
  font-weight: bolder;
  color: black;
  font-size: 18px;
}

.footer-bottom {
  border-radius: 20px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px,
    rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
  padding: 4px 10px;
  font-size: 14px;
  margin-top: 4px;
}

.footer-right {
  display: flex;
  align-items: center;
  gap: 10px;
}

.submit {
  border-radius: 20px;
  padding: 2px 14px;
  background-color: #f38245;
  color: white;
  font-size: 12px;
}

.club-icon {
  width: 50px;
  height: 40px;
}

.heading {
  font-size: larger;
  font-weight: bolder;
}
.link {
  font-size: 12.5px;
}
</style>
