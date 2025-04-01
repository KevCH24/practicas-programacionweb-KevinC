<script setup> 
import { ref } from 'vue' // Importo ref para variables reactivas
import Hijo1 from './Hijo1.vue' // Importo el componente Hijo1
import Hijo2 from './Hijo2.vue' // Importo el componente Hijo2

// Defino la propiedad 'nombre' que este componente espera recibir
defineProps({
  nombre: String,
})
</script>

<template>
  <br>
  <div class="container">
    <!-- Título del componente padre -->
    <h1 class="title rounded-lg">
      <i class="fas fa-user"></i>
      Soy el componente padre
    </h1>
    
    <!-- Renderizo el componente Hijo1 y le paso la propiedad 'edad' -->
    <div class="hijo-icon">
      <i class="fas fa-child"></i>
      <Hijo1 class="mt-4 rounded-lg" edad="---10"/>
    </div>

    <!-- Renderizo el componente Hijo2 y le paso la propiedad 'edad' -->
    <div class="hijo-icon">
      <i class="fas fa-child"></i>
      <Hijo2 class="mt-4 rounded-lg" edad="---5"/>
    </div>
  </div>
</template>