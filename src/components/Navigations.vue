<script setup>
import { reactive, ref } from "vue";
import discount from "/images/discount.png";
import customer from "/images/customer.png";
import home from "/images/home.png";
import sponsor from "/images/sponsor.png";
import profile from "/images/profile.png";

const navButtons = reactive([
  {
    icon: discount,
    text: "优惠",
  },
  {
    icon: customer,
    text: "窨服",
  },
  {
    icon: home,
    text: "",
  },
  {
    icon: sponsor,
    text: "赞助",
  },
  {
    icon: profile,
    text: "我的",
  },
]);
const activeIndex = ref(2);
</script>

<template>
  <div class="navigations">
    <button
      v-for="(btn, index) in navButtons"
      :key="index"
      class="btn"
      @click="activeIndex = index"
    >
      <img :class="index === 2 && 'home'" :src="btn.icon" alt="icon" />
      <div>{{ btn.text }}</div>
    </button>
  </div>
</template>

<style scoped>
.navigations {
  border-radius: 20px 20px 0 0;
  background-color: white;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 6px 0;
  position: fixed !important;
  width: 100vw;
  bottom: 0;
  box-shadow: 0 0 5px 2px hsla(0, 0%, 65.5%, 0.4);
  z-index: 200;
}
.btn {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1px;
  font-size: 14px;
  border: none;
  background-color: white;
}
.home {
  width: 75px;
  width: 75px;
  margin-top: -15px;
}
img {
  width: 30px;
}
</style>
