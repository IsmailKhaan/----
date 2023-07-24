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
    text: "喂养",
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
      :class="index === activeIndex ? 'active' : ''"
      @click="activeIndex = index"
    >
      <img :src="btn.icon" alt="icon" />
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
  padding: 4px;
  position: sticky;
  bottom: 0;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
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
.active {
  background-color: #f38245;
  border-radius: 100%;
  height: 70px;
  width: 70px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: solid 2px wheat;
  color: white;
  margin-top: -20px;
  outline: none;
}
img {
  width: 30px;
}
</style>
