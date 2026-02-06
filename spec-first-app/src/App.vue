<template>
  <div id="app">
    <h1>Team Members</h1>
    <div class="cards-grid">
      <UserCard name="BTK" role="Frontend Developer" />
      <UserCard name="John" role="Backend Engineer" />
      <UserCard name="BOb" role="UI/UX Designer" />
    </div>
  </div>
</template>

<script setup>
import UserCard from './components/UserCard.vue'
</script>

<style scoped>
#app {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
  text-align: center;
}

h1 {
  font-size: 32px;
  color: #1f2937;
  margin-bottom: 40px;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 24px;
}
</style>


