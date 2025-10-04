<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 9: Watchers</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-9" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Observadores (Watchers)</h2>
            <p class="mb-3">
              ID de TODO: <input v-model.number="todoId" type="number" class="form-control d-inline-block w-auto">
            </p>
            <p v-if="loading" class="alert alert-info">
              <span class="spinner-border spinner-border-sm me-2"></span>
              Cargando...
            </p>
            <div v-else-if="todoData" class="alert alert-success">
              <strong>{{ todoData.title }}</strong>
              <p class="mb-0 mt-2">Completado: {{ todoData.completed ? '✅' : '❌' }}</p>
            </div>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Los watchers permiten ejecutar efectos secundarios cuando los datos reactivos cambian.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'

const todoId = ref(1)
const todoData = ref(null)
const loading = ref(false)

async function fetchData() {
  loading.value = true
  todoData.value = null
  try {
    const res = await fetch(`https://jsonplaceholder.typicode.com/todos/${todoId.value}`)
    todoData.value = await res.json()
  } catch (error) {
    console.error('Error fetching data:', error)
  } finally {
    loading.value = false
  }
}

watch(todoId, fetchData, { immediate: true })
</script>
