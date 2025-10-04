<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <div class="container-fluid">
        <NuxtLink to="/" class="navbar-brand">
          <i class="bi bi-mortarboard-fill me-2"></i>
          Tutorial Vue con Nuxt
        </NuxtLink>
        <button 
          class="navbar-toggler" 
          type="button" 
          data-bs-toggle="collapse" 
          data-bs-target="#navbarNav"
          aria-controls="navbarNav" 
          aria-expanded="false" 
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item dropdown">
              <a 
                class="nav-link dropdown-toggle" 
                href="#" 
                id="leccionesDropdown" 
                role="button" 
                data-bs-toggle="dropdown" 
                aria-expanded="false"
              >
                <i class="bi bi-book me-1"></i>
                Lecciones
              </a>
              <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="leccionesDropdown">
                <li v-for="n in 15" :key="n">
                  <NuxtLink 
                    :to="`/leccion-${String(n).padStart(2, '0')}`" 
                    class="dropdown-item"
                  >
                    Lección {{ n }}
                  </NuxtLink>
                </li>
              </ul>
            </li>
            <li class="nav-item">
              <a 
                class="nav-link" 
                href="https://vuejs.org/tutorial/" 
                target="_blank"
                rel="noopener noreferrer"
              >
                <i class="bi bi-box-arrow-up-right me-1"></i>
                Tutorial Oficial
              </a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    
    <main class="container-fluid py-4">
      <slot />
    </main>
    
    <footer class="bg-light text-center py-3 mt-5">
      <div class="container">
        <p class="text-muted mb-0">
          <i class="bi bi-github me-2"></i>
          Tutorial Vue con Nuxt - 15 Lecciones
        </p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.navbar-brand {
  font-weight: 600;
}

.dropdown-menu {
  max-height: 400px;
  overflow-y: auto;
}

main {
  min-height: calc(100vh - 200px);
}
</style>
