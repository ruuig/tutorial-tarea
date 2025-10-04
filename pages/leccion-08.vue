<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 8: Lifecycle and Template Refs</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-8" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Ciclo de Vida y Referencias de Plantilla</h2>
            <p ref="pRef" class="alert alert-primary">Hola</p>
            <button @click="focusInput" class="btn btn-primary mb-3">
              <i class="bi bi-cursor-text me-2"></i>
              Enfocar Input
            </button>
            <input ref="inputRef" class="form-control" placeholder="Haz clic en el botón para enfocar">
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Usa <code>ref</code> para acceder a elementos del DOM y hooks de ciclo de vida como <code>onMounted</code>.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const pRef = ref(null)
const inputRef = ref(null)

onMounted(() => {
  if (pRef.value) {
    pRef.value.textContent = 'Montado!'
  }
})

function focusInput() {
  inputRef.value?.focus()
}
</script>
