<script setup>
import { ref } from 'vue'
const binevenida = ref ("Binevenidos a la seccion de condicionales");
const nombre = ref ("Kevin");
const apellidos = ref("Cruz Hernandez")
//defineProps({
  //msg: String,
//})


</script>

<template>
  <div class="container">
    <h2 class="text-center">{{ binevenida }}</h2>
<div class="row">
  <div class="col-md-6">
    <h6>{{ nombre }}</h6>
    <h6>{{ apellidos }}</h6>
  </div>
</div>
  </div>
</template>

<style scoped>
</style>