<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 7: Computed Property</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-7" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Propiedades Computadas</h2>
            <ul class="list-group mb-3">
              <li 
                v-for="todo in todos" 
                :key="todo.id" 
                class="list-group-item d-flex align-items-center"
              >
                <input 
                  type="checkbox" 
                  v-model="todo.done" 
                  class="form-check-input me-2"
                >
                <span :class="{ 'text-decoration-line-through text-muted': todo.done }">
                  {{ todo.text }}
                </span>
              </li>
            </ul>
            <p class="alert alert-info">
              Tareas pendientes: <strong>{{ hideCompleted ? filteredTodos.length : activeTodoCount }}</strong>
            </p>
            <div class="form-check">
              <input 
                type="checkbox" 
                v-model="hideCompleted" 
                class="form-check-input" 
                id="hideCompleted"
              >
              <label class="form-check-label" for="hideCompleted">
                Ocultar completadas
              </label>
            </div>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Las propiedades computadas se recalculan automáticamente cuando sus dependencias cambian.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const hideCompleted = ref(false)
const todos = ref([
  { id: 1, text: 'Aprender Vue', done: true },
  { id: 2, text: 'Construir algo increíble', done: false },
  { id: 3, text: 'Compartir con el mundo', done: false }
])

const filteredTodos = computed(() => {
  return hideCompleted.value
    ? todos.value.filter(t => !t.done)
    : todos.value
})

const activeTodoCount = computed(() => {
  return todos.value.filter(t => !t.done).length
})
</script>
