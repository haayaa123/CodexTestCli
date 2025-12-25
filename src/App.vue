<script setup>
import { ref, watch } from 'vue'

const STORAGE_KEY = 'counter'
const count = ref(0)

const saved = localStorage.getItem(STORAGE_KEY)
const initial = Number(saved)
if (!Number.isNaN(initial)) {
  count.value = initial
}

watch(count, (value) => {
  localStorage.setItem(STORAGE_KEY, String(value))
})

const increment = () => {
  count.value += 1
}

const decrement = () => {
  count.value -= 1
}

const reset = () => {
  count.value = 0
}
</script>

<template>
  <main class="counter">
    <h1>Counter</h1>
    <div class="value">{{ count }}</div>
    <div class="actions">
      <button type="button" @click="decrement">-1</button>
      <button type="button" @click="increment">+1</button>
      <button type="button" @click="reset">Reset</button>
    </div>
  </main>
</template>

<style scoped>
.counter {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.value {
  font-size: 3rem;
  font-weight: 700;
}

.actions {
  display: flex;
  gap: 0.75rem;
}
</style>
