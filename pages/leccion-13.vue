<template>
  <div>
    <ChildComp>
      This is some slot content!
    </ChildComp>
  </div>
</template>

<script setup>
const ChildComp = {
  template: `
    <div>
      <slot>Fallback content</slot>
    </div>
  `
}
</script>
