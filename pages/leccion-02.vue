<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 2: Attribute Bindings</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-2" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Vinculación de Atributos</h2>
            <p :id="dynamicId" :class="dynamicClass">Este párrafo tiene atributos dinámicos</p>
            <p class="text-muted small">ID: {{ dynamicId }}, Class: {{ dynamicClass }}</p>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Usa <code>v-bind:</code> o <code>:</code> para vincular atributos HTML a datos reactivos.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const dynamicId = ref('my-id')
const dynamicClass = ref('text-primary fw-bold')
</script>
