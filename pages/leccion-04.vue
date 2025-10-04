<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 4: Form Bindings</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-4" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Vinculación de Formularios</h2>
            <div class="mb-3">
              <input 
                v-model="text" 
                class="form-control" 
                placeholder="Escribe algo..."
              >
            </div>
            <p class="alert alert-secondary">{{ text }}</p>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> <code>v-model</code> crea vinculación bidireccional en elementos de formulario.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const text = ref('')
</script>
