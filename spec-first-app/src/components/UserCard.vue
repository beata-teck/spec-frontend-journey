<template>
  <div class="user-card">
    <div class="avatar">{{ name.split(' ').map(n => n[0]).join('') }}</div>
    <div class="info">
      <h3 class="name">{{ name }}</h3>
      <p class="role">{{ role }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  name: {
    type: String,
    required: true
  },
  role: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.user-card {
  display: grid;
  grid-template-columns: auto 1fr;
  align-items: center;
  gap: 16px;
  padding: 20px;
  border: 2px solid #e5e7eb;
  border-radius: 12px;
  background: white;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: all 0.2s;
  max-width: 350px;
}

.user-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}

.avatar {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: linear-gradient(135deg, #3b82f6, #1d4ed8);
  color: white;
  display: grid;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  font-size: 24px;
}

.info {
    text-align: left;
}

.name {
  margin: 0 0 4px 0;
  font-size: 20px;
  color: #111827;
}

.role {
  margin: 0;
  color: #6b7280;
  font-size: 16px;
  font-weight: 500;
}
</style>
