<script setup>
import { ref } from 'vue' // Importo ref para variables reactivas

// Defino la propiedad 'edad' que se recibe desde el padre
defineProps({
  edad: String,
})
</script>

<template>
  <!-- Contenido del componente hijo2 -->
  <h6> Soy el componente Hijo 2 </h6>
  <p>{{ edad }}</p>
</template>

<style scoped> </style>