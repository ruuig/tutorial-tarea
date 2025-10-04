<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 13: Slots</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-13" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm">
          <div class="card-body">
            <h2 class="h4 mb-3">Slots</h2>
            <ChildComp>
              <template #default>
                <p class="text-primary fw-bold">Este es el contenido del slot por defecto</p>
              </template>
            </ChildComp>
          </div>
        </div>

        <div class="alert alert-info mt-4">
          <strong>Concepto:</strong> Los slots permiten al padre pasar contenido de plantilla al hijo.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const ChildComp = {
  template: `
    <div class="alert alert-success">
      <strong>Componente Hijo con Slot:</strong>
      <div class="mt-2">
        <slot>Contenido por defecto si no se proporciona slot</slot>
      </div>
    </div>
  `
}
</script>
