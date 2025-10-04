# Instrucciones para subir a GitHub

## Pasos para crear el repositorio público y hacer push

### 1. Crear repositorio en GitHub
1. Ve a https://github.com/new
2. Nombre del repositorio: `tutorial-nuxt-rudy` (o el nombre que prefieras)
3. Descripción: "Tutorial Vue.js con Nuxt 3 - 15 Lecciones"
4. Selecciona **Público**
5. **NO** inicialices con README, .gitignore o licencia (ya los tenemos)
6. Haz clic en "Create repository"

### 2. Conectar y hacer push
Después de crear el repo, GitHub te mostrará comandos. Usa estos (reemplaza `TU-USUARIO` con tu usuario de GitHub):

```bash
git remote add origin https://github.com/TU-USUARIO/tutorial-nuxt-rudy.git
git push -u origin main
```

### Comandos completos desde PowerShell:
```powershell
cd C:\Users\Rudy\CascadeProjects\nuxt-vue-tutorial-curso
git remote add origin https://github.com/TU-USUARIO/tutorial-nuxt-rudy.git
git push -u origin main
```

## Verificación
- El archivo `.gitignore` ya está configurado para excluir `node_modules`
- Todos los archivos del proyecto están en el commit inicial
- El branch principal es `main`

## Para ejecutar el proyecto localmente:
```bash
npm run dev
```

Luego abre http://localhost:3000 en tu navegador.

## Estructura del proyecto
- `/pages/index.vue` - Página principal con lista de lecciones
- `/pages/leccion-01.vue` a `/pages/leccion-15.vue` - Las 15 lecciones
- `/layouts/default.vue` - Layout con navbar Bootstrap
- `/plugins/bootstrap.client.ts` - Plugin para Bootstrap JS
- `nuxt.config.ts` - Configuración de Nuxt con Bootstrap CSS
