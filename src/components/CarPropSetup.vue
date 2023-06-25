<template>
  <div>
    <h1>Verificación CAR Composition</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ props.power }}</p>
    <button @click="props.upPower">Aumenta</button>
  </div>
</template>
<script setup>
import { ref } from "vue";
const brand = "Audi";
const model = "A4";
const props = defineProps({
  power: {
    type: Number,
    default: 60,
  },
  upPower: {
    type: Function,
    default: () => {
      return "Prueba de función";
    },
  },
});
console.log("Props setup: ", props);
function testPower() {
  props.upPower();
}
</script>

<style lang="scss" scoped></style>
