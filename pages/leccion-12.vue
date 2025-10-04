<template>
  <div>
    <ChildComp @response="(msg) => childMsg = msg" />
    <p>{{ childMsg }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const childMsg = ref('No child msg yet')

const ChildComp = {
  emits: ['response'],
  template: `
    <button @click="$emit('response', 'hello from child')">
      Click me
    </button>
  `
}
</script>
