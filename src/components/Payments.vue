<script setup>
const props = defineProps({
  icon: String,
  text: String,
});
</script>

<template>
  <div class="icon-btn">
    <img :src="props.icon" alt="icon" />
    <div>{{ props.text }}</div>
  </div>
</template>

<style scoped>
.icon-btn {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 2px;
  font-size: 12px;
}
</style>
