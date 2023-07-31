<script setup>
import { reactive, ref, watch } from "vue";
import footballtab from "/images/footballtab.png";
import footballtab_active from "/images/footballtab_active.png";
import gamestab from "/images/gamestab.png";
import gamestab_active from "/images/gamestab_active.png";
import ludotab from "/images/ludotab.png";
import ludotab_active from "/images/ludotab_active.png";
import chesstab from "/images/chesstab.png";
import chesstab_active from "/images/chesstab_active.png";
import spottab from "/images/spottab.png";
import spottab_active from "/images/spottab_active.png";
import pooltab from "/images/pooltab.png";
import pooltab_active from "/images/pooltab_active.png";

const props = defineProps({
  scrollValue: Object,
});

const emit = defineEmits(["handleSetScrollMargin"]);

const buttons = reactive([
  {
    icon: footballtab,
    activeIcon: footballtab_active,
    scrollMargin: 0,
  },
  {
    icon: gamestab,
    activeIcon: gamestab_active,
    scrollMargin: 371,
  },
  {
    icon: ludotab,
    activeIcon: ludotab_active,
    scrollMargin: 761,
  },
  {
    icon: chesstab,
    activeIcon: chesstab_active,
    scrollMargin: 1141,
  },
  {
    icon: spottab,
    activeIcon: spottab_active,
    scrollMargin: 1531,
  },
  {
    icon: pooltab,
    activeIcon: pooltab_active,
    scrollMargin: 1911,
  },
]);
const activeIndex = ref(0);

watch(
  () => props.scrollValue.value,
  (scrollValue) => {
    console.log("Scroll Value:", scrollValue);
    switch (true) {
      case scrollValue > 1910:
        activeIndex.value = 5;
        break;
      case scrollValue > 1530:
        activeIndex.value = 4;
        break;
      case scrollValue > 1140:
        activeIndex.value = 3;
        break;
      case scrollValue > 760:
        activeIndex.value = 2;
        break;
      case scrollValue > 370:
        activeIndex.value = 1;
        break;
      default:
        activeIndex.value = 0;
    }
  }
);
</script>

<template>
  <div class="player-menu">
    <div
      v-for="(btn, index) in buttons"
      :key="index"
      @click="
        activeIndex = index;
        emit('handleSetScrollMargin', btn.scrollMargin);
      "
    >
      <img
        :src="index === activeIndex ? btn.activeIcon : btn.icon"
        alt="icon"
      />
    </div>
  </div>
</template>

<style scoped>
.player-menu {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 6px;
}
img {
  width: 54px;
  height: 68px;
}
</style>
