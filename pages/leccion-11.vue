<template>
  <div>
    <ChildComp :msg="greeting" />
  </div>
</template>

<script setup>
import { ref } from 'vue'

const greeting = ref('Hello from parent')

const ChildComp = {
  props: {
    msg: String
  },
  template: `<h2>{{ msg || 'No props passed yet' }}</h2>`
}
</script>
