<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 14: Provide / Inject</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-14" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Provide / Inject</h2>
            <ParentComp />
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Provide/Inject permite pasar datos a través de múltiples niveles de componentes.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { provide, inject } from 'vue'

const ParentComp = {
  setup() {
    provide('message', 'Mensaje desde el ancestro')
    return {}
  },
  template: `
    <div class="alert alert-primary">
      <strong>Componente Padre</strong>
      <ChildComp />
    </div>
  `
}

const ChildComp = {
  setup() {
    const message = inject('message')
    return { message }
  },
  template: `
    <div class="alert alert-success mt-2">
      <strong>Componente Hijo:</strong> {{ message }}
    </div>
  `
}
</script>
