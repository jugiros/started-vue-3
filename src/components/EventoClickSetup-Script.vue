<template>
  <h1>Verificación objeto click</h1>
  <h2>{{ text }}</h2>
  <button @click="clickInit()">Validar</button>
</template>

<script setup>
import {onMounted} from "vue";

const text = 'prueba';
function clickInit() {
  alert('Prueba de click inicial')
}
// onMounted(() => {
//   alert('Inicio de la vista')
// })
</script>

<style scoped></style>
