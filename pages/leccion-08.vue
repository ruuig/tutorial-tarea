<template>
  <div>
    <p ref="pRef">hello</p>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const pRef = ref(null)

onMounted(() => {
  pRef.value.textContent = 'mounted!'
})
</script>
