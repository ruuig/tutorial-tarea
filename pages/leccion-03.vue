<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 3: Event Listeners</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-3" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Escuchadores de Eventos</h2>
            <p class="display-6">{{ count }}</p>
            <button @click="increment" class="btn btn-primary">
              <i class="bi bi-plus-circle me-2"></i>
              Incrementar
            </button>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Usa <code>v-on:</code> o <code>@</code> para escuchar eventos del DOM.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}
</script>
