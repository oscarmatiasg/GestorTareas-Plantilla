<template>
  <div id="app">
    <!-- Barra de navegación con enlaces a diferentes rutas -->
    <nav class="navbar">
      <div class="navbar-container">
        <a class="navbar-brand" href="#">
          <span class="vue-icon">
            <!-- Logo de Vue en SVG -->
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 261.76 226.69" width="24" height="24">
              <path fill="#42b883" d="M130.88,0l-130.88,0l130.88,226.69l130.88-226.69h-52.352l-78.528,135.658l-78.528-135.658h-52.352l130.88,226.69l130.88-226.69h-52.352z"/>
              <path fill="#35495e" d="M0,0h52.352l78.528,135.658l78.528-135.658h52.352l-130.88,226.69l-130.88-226.69z"/>
            </svg>
          </span>
        <router-link to="/" class="nav-link">Gestor de Tareas</router-link>

        </a>
        <ul class="navbar-links">
          <li><router-link to="/addtask" class="nav-link">➕ Añadir Tarea</router-link></li>
          <li><router-link to="/tasklist" class="nav-link">📝 Lista de Tareas</router-link></li>
          <li><router-link to="/combinedview" class="nav-link">📋 Vista Combinada</router-link></li>
        </ul>
      </div>
    </nav>
    <!-- Aquí se cargará el componente correspondiente a la ruta seleccionada -->
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #f8f9fa;
}

.navbar {
  background-color: #007bff;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.navbar-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 800px;
  margin: 0 auto;
}

.navbar-brand {
  color: #f8f9fa;
  font-weight: bold;
  font-size: 18px;
  margin-right: 20px;
  text-decoration: none;
}

.vue-icon {
  margin-right: 10px;
}

.navbar-links {
  list-style: none;
  display: flex;
  justify-content: space-between;
  margin: 0;
  padding: 0;
}

.nav-link {
  color: #f8f9fa;
  font-weight: bold;
  text-decoration: none;
  margin: 0 20px;
}

.nav-link.router-link-exact-active {
  color: #a5d6a7;
}

@media (max-width: 768px) {
  .navbar-container {
    flex-direction: column;
    align-items: center;
  }
  .navbar-brand {
    margin-bottom: 10px;
  }
  .navbar-links {
    flex-direction: column;
  }
  .nav-link {
    margin: 10px 0;
  }
}
</style>