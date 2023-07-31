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
    <div class="carousel-section">
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
    </div>
    <div class="input">
      <img class="sound" :src="sound" alt="icon" />
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
  overflow: hidden;
  border-radius: 0 0 20px 20px;
  box-shadow: 0 5px 5px rgba(0, 0, 0, 0.1);
}
.logo {
  width: 106px;
  height: 24px;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px;
}
.carousel-section {
  padding: 0 12px;
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
.sound {
  width: 22px;
  height: 22px;
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
  margin: 0 12px;
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
  box-shadow: 0 5px 5px rgba(0, 0, 0, 0.1);
  margin-bottom: 4px;
  padding: 0 20px;
  padding-top: -20px;
  padding-bottom: 10px;
}
.footer-bottom {
  height: 30px;
  min-width: 100px;
  padding-top: 10px;
  color: #6d7ba8;
  font-size: 14px;
  border-radius: 50px;
  box-shadow: 0 2px 3px #d3deff;
  background: linear-gradient(180deg, #fcfeff, #f1f5fe);
  text-align: center;
}

.footer-right {
  display: flex;
  align-items: center;
  gap: 10px;
  color: black;
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
  height: 140px;
}

.swiper-slide img {
  width: 100%;
  height: 100%;
  border-radius: 14px;
  object-fit: cover;
  object-position: top;
}
</style>
