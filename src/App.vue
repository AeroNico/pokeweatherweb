<template>
  <div id="app">
    <!-- Mostrar la vista Home -->
    <Home />
  </div>
</template>

<script>
// Importar el componente Home
import Home from './views/HomeView.vue'

export default {
  name: 'App',
  components: {
    Home // Registrar el componente Home para usarlo en la plantilla
  }
}
</script>

<style>
/* Aquí van tus estilos globales */
</style>
