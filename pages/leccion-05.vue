<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 5: Conditional Rendering</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-5" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Renderizado Condicional</h2>
            <button @click="toggle" class="btn btn-primary mb-3">
              <i class="bi bi-eye me-2"></i>
              Toggle
            </button>
            <p v-if="awesome" class="alert alert-success">Vue es increíble!</p>
            <p v-else class="alert alert-warning">Oh no 😢</p>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Usa <code>v-if</code>, <code>v-else-if</code>, <code>v-else</code> para renderizado condicional.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const awesome = ref(true)

function toggle() {
  awesome.value = !awesome.value
}
</script>
