<template>
  <div id="app">
    <h1>Counter</h1>
    <div class="counter">
      <button 
        @click="decrement" 
        :disabled="count === 0"
        class="btn btn-minus"
      >
        –
      </button>
      
      <div class="display">
        <span class="count">{{ count }}</span>
      </div>
      
      <button @click="increment" class="btn btn-plus">
        +
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)  // Reactive counter

const increment = () => {
  count.value++
}

const decrement = () => {
  if (count.value > 0) {
    count.value--
  }
}
</script>

<style scoped>
#app {
  max-width: 400px;
  margin: 50px auto;
  text-align: center;
  font-family: system-ui;
}

h1 {
  color: #1f2937;
  margin-bottom: 40px;
}

.counter {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  padding: 40px;
  background: linear-gradient(135deg, #f8fafc, #e2e8f0);
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}

.display {
  background: white;
  width: 120px;
  height: 120px;
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 8px 20px rgba(0,0,0,0.1);
  font-size: 48px;
  font-weight: bold;
  color: #1e40af;
}

.btn {
  width: 60px;
  height: 60px;
  border: none;
  border-radius: 50%;
  font-size: 24px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.2s;
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.btn-plus {
  background: #10b981;
  color: white;
}

.btn-plus:hover:not(:disabled) {
  background: #059669;
  transform: scale(1.05);
}

.btn-minus {
  background: #ef4444;
  color: white;
}

.btn-minus:hover:not(:disabled) {
  background: #dc2626;
  transform: scale(1.05);
}

.btn:disabled {
  background: #9ca3af;
  cursor: not-allowed;
  transform: none;
}
</style>




