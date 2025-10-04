<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 6: List Rendering</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-6" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Renderizado de Listas</h2>
            <ul class="list-group">
              <li v-for="todo in todos" :key="todo.id" class="list-group-item">
                {{ todo.text }}
              </li>
            </ul>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Usa <code>v-for</code> para renderizar listas de elementos.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const todos = ref([
  { id: 1, text: 'Aprender Vue' },
  { id: 2, text: 'Construir algo increíble' },
  { id: 3, text: 'Compartir con el mundo' }
])
</script>
