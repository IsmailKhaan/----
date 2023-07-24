<script setup>
const props = defineProps({
  title: String,
  icon: String,
  name: String,
  club: String,
  image: String,
});
</script>

<template>
  <div class="player-card">
    <div class="tag">{{ props.title }}</div>
    <div class="card">
      <div class="card-left">
        <img class="club-icon" :src="props.icon" alt="icon" />
        <div class="name">{{ props.name }}</div>
        <div class="club">-{{ props.club }}-</div>
      </div>
      <div class="card-right">
        <img class="player-image" :src="props.image" alt="image" />
      </div>
    </div>
  </div>
</template>

<style>
.player-card {
  height: 160px;
  width: 265px;
  background: #eff1fe;
  border-radius: 16px;
  display: flex;
  flex-direction: column;
  border: solid 2px white;
}
.tag {
  background-color: #f38245;
  width: fit-content;
  color: white;
  padding: 2px 20px;
  font-size: 12px;
  border-radius: 16px 0 16px 0;
  margin-top: -2px;
  margin-left: -2px;
}
.card {
  display: flex;
}
.card-left {
  width: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 5px;
}

.card-right {
  width: 50%;
  margin-top: 20px;
  background-image: url("/images/sports.png");
  background-repeat: no-repeat;
}

.player-image {
  width: 150px;
  height: 140px;
  margin-top: -20px;
  object-fit: contain;
}
.name {
  font-weight: bolder;
  color: black;
  font-size: 18px;
}
.club {
  font-size: 12px;
}
.club-icon {
  width: 40px;
}
</style>
