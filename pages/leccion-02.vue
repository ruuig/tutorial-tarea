<template>
  <div>
    <h1 :class="titleClass">Make me red</h1>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
</script>

<style>
.title {
  color: red;
}
</style>
