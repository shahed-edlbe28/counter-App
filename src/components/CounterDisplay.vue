<template>
  <div>
    <h2>Counter Display</h2>

    <p>Count: {{ counter.count }}</p>
    <p>Double: {{ counter.doubleCount }}</p>
  </div>
</template>

<script setup>
import { useCounterStore } from '../stores/counter'

const counter = useCounterStore()
</script>