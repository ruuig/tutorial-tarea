<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 11: Props</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-11" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Props</h2>
            <ChildComp 
              :msg="greeting" 
              :count="count"
            />
            <button @click="count++" class="btn btn-primary mt-3">
              <i class="bi bi-plus-circle me-2"></i>
              Incrementar
            </button>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Las props permiten pasar datos del componente padre al hijo.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const greeting = ref('Hola desde el padre')
const count = ref(0)

const ChildComp = {
  props: {
    msg: String,
    count: Number
  },
  template: `
    <div class="alert alert-primary">
      <p><strong>Mensaje:</strong> {{ msg }}</p>
      <p class="mb-0"><strong>Contador:</strong> {{ count }}</p>
    </div>
  `
}
</script>
