<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 1: Declarative Rendering</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-1" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Renderizado Declarativo</h2>
            <p>{{ message }}</p>
            <p>Count is: {{ counter.count }}</p>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Vue usa sintaxis de plantilla para renderizar datos reactivos.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const message = ref('Hello World!')
const counter = reactive({ count: 0 })
</script>
