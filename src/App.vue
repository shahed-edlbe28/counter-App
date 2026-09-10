<template>
  <div class="app">
    <div class="counter-card">
    <h1>Counter</h1>

    <p class="count-display">{{ counter.count }}</p>

    <input
    class="count-input"
    type="number"
    v-model="counter.count"
      >

   <p class="double-count">
    Double Count: <strong>{{ counter.doubleCount }}</strong>
    </p>
    <div class="buttons">
    <button class="btn decrease" @click="counter.decrement">-</button>
    <button class="btn increase" @click="counter.increment">+</button>
    </div>
    <CounterDisplay />
     </div>
  </div>
</template>

<script setup>
import { useCounterStore } from './stores/counter'
import CounterDisplay from './components/CounterDisplay.vue'

const counter = useCounterStore()
</script>