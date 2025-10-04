<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="mb-4">
          <h1 class="display-5 fw-bold text-primary">Lección 15: You Did It!</h1>
          <p class="text-muted">
            <a href="https://vuejs.org/tutorial/#step-15" target="_blank" rel="noopener noreferrer">
              Ver en Tutorial Oficial <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </p>
        </div>

        <div class="card shadow-sm border-success">
          <div class="card-body text-center">
            <h2 class="h3 mb-4 text-success">
              <i class="bi bi-trophy-fill me-2"></i>
              ¡Felicitaciones!
            </h2>
            <p class="lead">Has completado el tutorial de Vue.js</p>
            <p class="text-muted">
              Ahora tienes los fundamentos para construir aplicaciones Vue increíbles.
            </p>
            
            <div class="alert alert-info mt-4 text-start">
              <h4 class="h5">
                <i class="bi bi-lightbulb-fill me-2"></i>
                Próximos pasos
              </h4>
              <ul class="mb-0">
                <li>Explora la <a href="https://vuejs.org/guide/" target="_blank">Guía de Vue</a></li>
                <li>Lee la <a href="https://nuxt.com/docs" target="_blank">Documentación de Nuxt</a></li>
                <li>Construye tu primer proyecto real</li>
                <li>Únete a la comunidad de Vue</li>
              </ul>
            </div>

            <div class="mt-4">
              <NuxtLink to="/" class="btn btn-primary btn-lg">
                <i class="bi bi-house-fill me-2"></i>
                Volver al Inicio
              </NuxtLink>
            </div>
          </div>
        </div>

        <div class="alert alert-success mt-4">
          <strong>Concepto:</strong> ¡Has aprendido los conceptos fundamentales de Vue! Sigue practicando y construyendo.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// ¡Felicitaciones por completar el tutorial!
</script>
