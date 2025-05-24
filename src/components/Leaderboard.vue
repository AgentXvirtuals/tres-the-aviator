<script setup lang="ts">
const players = [
  { name: 'Player1', score: 9850 },
  { name: 'Player2', score: 8720 },
  { name: 'Player3', score: 7650 },
  { name: 'Player4', score: 6540 },
  { name: 'Player5', score: 5430 },
]
</script>

<template>
  <div class="leaderboard">
    <h3>Leaderboard</h3>
    <div class="leaderboard-list">
      <div v-for="(player, index) in players" :key="index" class="leaderboard-item">
        <span class="rank">{{ index + 1 }}</span>
        <span class="name">{{ player.name }}</span>
        <span class="score">{{ player.score }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.leaderboard {
  position: fixed;
  left: 20px;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0, 0, 0, 0.7);
  padding: 15px;
  border-radius: 10px;
  color: white;
  min-width: 200px;
}

.leaderboard h3 {
  text-align: center;
  margin-bottom: 15px;
  color: #68c3c0;
  font-size: 1.2em;
}

.leaderboard-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.leaderboard-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 5px 10px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 5px;
}

.rank {
  color: #d1b790;
  font-weight: bold;
}

.name {
  flex: 1;
  margin: 0 10px;
}

.score {
  color: #68c3c0;
  font-weight: bold;
}
</style> 