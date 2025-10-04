<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 10: Components</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-10" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Componentes</h2>
            <ChildComp msg="Mensaje desde el padre" />
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Los componentes permiten dividir la UI en piezas reutilizables e independientes.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const ChildComp = {
  props: ['msg'],
  template: `<div class="alert alert-success"><strong>Componente Hijo:</strong> {{ msg }}</div>`
}
</script>
