<script setup>
import { ref, onMounted } from "vue";
import SelectionMenu from "./SelectionMenu.vue";
import PlayersSection from "./PlayersSection.vue";

const scrollDivRef = ref(null);
const scrollValue = ref({ value: 0 });
const scrollMargin = ref(0);

const updateScrollValue = () => {
  if (scrollDivRef.value) {
    scrollValue.value.value = scrollDivRef.value.scrollTop;
  }
};
const scrollPlayersSection = () => {
  if (scrollDivRef.value) {
    scrollDivRef.value.scrollTop;
    const targetPosition = scrollMargin.value;
    const options = {
      top: targetPosition,
    };
    scrollDivRef.value.scrollTo(options);
  }
};
onMounted(() => {
  scrollDivRef.value = document.querySelector(".scroll");
});
const handleSetScrollMargin = (value) => {
  scrollMargin.value = value;
};
</script>

<template>
  <div class="view-player">
    <div class="menu_scroll" @click="scrollPlayersSection">
      <SelectionMenu
        :scrollValue="scrollValue"
        @handleSetScrollMargin="handleSetScrollMargin"
      />
    </div>
    <div class="scroll" ref="scrollDiv" @scroll="updateScrollValue">
      <PlayersSection />
    </div>
  </div>
</template>

<style scoped>
.view-player {
  display: flex;
  justify-content: space-between;
  align-items: start;
  padding: 10px;
  gap: 8px;
}
.scroll,
.menu_scroll {
  height: 40vh;
  overflow-y: auto;
}
</style>
