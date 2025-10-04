<template>
  <div>
    <Child />
  </div>
</template>

<script setup>
import { ref, provide, inject } from 'vue'

const msg = ref('hello')
provide('message', msg)

const Child = {
  setup() {
    const message = inject('message')
    return { message }
  },
  template: `<p>Message to child: {{ message }}</p>`
}
</script>
