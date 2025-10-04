<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 12: Emits</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-12" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Emits</h2>
            <p class="display-6 mb-3">{{ count }}</p>
            <ChildComp @increment="count++" />
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Los componentes hijos pueden emitir eventos personalizados al padre.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

const ChildComp = {
  emits: ['increment'],
  template: `
    <button @click="$emit('increment')" class="btn btn-success">
      <i class="bi bi-arrow-up-circle me-2"></i>
      Incrementar desde hijo
    </button>
  `
}
</script>
