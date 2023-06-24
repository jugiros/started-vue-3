<template>
  <div>
    <h1>Verificación CAR Composition</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ props.power }}</p>
  </div>
</template>
<script setup>
import { ref } from "vue";
const brand = "Audi";
const model = "A4";
const props = defineProps({
  power: {
    type: String,
    default: 60,
  },
});
console.log("Props setup: ", props.power);
</script>

<style lang="scss" scoped></style>
