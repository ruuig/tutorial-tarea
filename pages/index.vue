<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-10">
        <div class="text-center mb-5">
          <h1 class="display-4 fw-bold text-primary mb-3">
            <i class="bi bi-mortarboard-fill me-3"></i>
            Tutorial Vue con Nuxt
          </h1>
          <p class="lead text-muted">
            15 Lecciones del Tutorial Oficial de Vue.js implementadas en Nuxt 3
          </p>
        </div>

        <div class="card shadow-sm mb-4">
          <div class="card-body">
            <h2 class="card-title h4 mb-3">
              <i class="bi bi-info-circle-fill text-info me-2"></i>
              Acerca de este proyecto
            </h2>
            <p class="card-text">
              Este proyecto contiene las 15 lecciones del 
              <a href="https://vuejs.org/tutorial/" target="_blank" rel="noopener noreferrer">
                Tutorial Oficial de Vue.js
              </a>
              implementadas en Nuxt 3 con Bootstrap 5.
            </p>
            <p class="card-text">
              Cada lección está disponible en una ruta separada y puede accederse desde el menú desplegable 
              <strong>"Lecciones"</strong> en la barra de navegación.
            </p>
          </div>
        </div>

        <div class="row g-3">
          <div class="col-md-4" v-for="n in 15" :key="n">
            <div class="card h-100 hover-shadow">
              <div class="card-body">
                <h5 class="card-title">
                  <i class="bi bi-journal-code text-primary me-2"></i>
                  Lección {{ n }}
                </h5>
                <p class="card-text text-muted small">
                  Ejercicio {{ n }} del tutorial oficial de Vue.js
                </p>
                <NuxtLink 
                  :to="`/leccion-${String(n).padStart(2, '0')}`" 
                  class="btn btn-outline-primary btn-sm"
                >
                  Ver Lección
                  <i class="bi bi-arrow-right ms-1"></i>
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>

        <div class="alert alert-info mt-5" role="alert">
          <h4 class="alert-heading">
            <i class="bi bi-lightbulb-fill me-2"></i>
            Instrucciones
          </h4>
          <p class="mb-0">
            Navega por las lecciones usando el menú desplegable en la barra de navegación 
            o haciendo clic en las tarjetas de arriba. Cada lección corresponde a un paso 
            del tutorial oficial de Vue.js.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hover-shadow {
  transition: box-shadow 0.3s ease;
}

.hover-shadow:hover {
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important;
}
</style>
