<script setup>
import { reactive } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/autoplay";
import Payments from "./Payments.vue";
import deposite from "/images/deposite.png";
import transfer from "/images/transfer.png";
import withdraw from "/images/withdraw.png";
import vip from "/images/vip.png";
import speak from "/images/speak.png";
import sound from "/images/sound.png";
import cover_1 from "/images/cover_1.jpg";
import cover_2 from "/images/cover_2.jpg";
import cover_3 from "/images/cover_3.jpg";
import cover_4 from "/images/cover_4.jpg";
import cover_5 from "/images/cover_5.jpg";
import xunli_logo from "/images/xunli_logo.png";

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
const photos = reactive([cover_1, cover_2, cover_3, cover_4, cover_5]);
</script>

<template>
  <div class="hero-section">
    <div class="header">
      <img class="logo" :src="xunli_logo" alt="xunli_logo" />
      <img class="header-right" :src="speak" alt="icon" />
    </div>
    <!-- <img class="carousel" :src="cover" alt="cover" /> -->
    <Swiper
      :modules="[Pagination, Autoplay]"
      :grab-cursor="true"
      :loop="true"
      :pagination="{ clickable: true }"
      :autoplay="{ delay: 2000, disableOnInteraction: false }"
    >
      <SwiperSlide v-for="photo in photos">
        <img class="carousel" :src="photo" alt="photo" />
      </SwiperSlide>
    </Swiper>
    <div class="input">
      <div class="sound-icon">
        <img :src="sound" alt="icon" />
      </div>
      <marquee scrollamount="10">测试滚动公告内容，欢迎来到汛利娱乐</marquee>
      <div class="submit">更多</div>
    </div>
    <div class="footer">
      <div class="footer-bottom">登录/注册</div>
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
  gap: 6px;
  background-color: white;
  padding: 12px;
  overflow: hidden;
  border-radius: 0 0 20px 20px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px,
    rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
}
.logo {
  width: 106px;
  height: 24px;
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
  background: linear-gradient(180deg, #feb68e, #f76f3f);
}
.header-left {
  display: flex;
  align-items: center;
  gap: 4px;
}

.header-right {
  width: 20px;
}

.input {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 4px;
  background-color: #f1f2f8;
  border-radius: 20px;
}

marquee {
  flex: 1;
  background: transparent;
  outline: none;
  border: none;
  padding: 2px;
  font-size: 12px;
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
  box-shadow: rgba(144, 169, 179, 0.25) 0px 6px 12px -2px,
    rgba(145, 97, 97, 0.3) 0px 3px 7px -3px;
  padding: 4px 40px;
  font-size: 14px;
  background-color: #f4f8fe;
}

.footer-right {
  display: flex;
  align-items: center;
  gap: 10px;
}

.submit {
  border-radius: 20px;
  padding: 2px 14px;
  background: linear-gradient(180deg, #feb68e, #f76f3f);
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

.swiper {
  width: 100%;
  height: 200px;
}

.swiper-slide img {
  width: 100%;
  height: 100%;
  border-radius: 14px;
  object-fit: cover;
  object-position: top;
}
</style>
