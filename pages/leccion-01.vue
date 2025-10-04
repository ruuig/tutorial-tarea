<template>
  <div>
    <h1>{{ message }}</h1>
    <p>Count is: {{ counter.count }}</p>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const message = ref('Hello World!')
const counter = reactive({ count: 0 })
</script>
