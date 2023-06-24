<template>
  <div>
    <h1>Verificación CAR Composition</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <button @click="upPower(20)">Aumentar</button>
    <button @click="downPower()">Disminuir</button>
    <p>Primer número: {{  }}</p>
  </div>
</template>
<script setup>
import { ref } from "vue";
const brand = "Audi";
const model = "A4";
let power = ref(40);

function upPower(val) {
  let newPower = power.value + val;
  power.value = power.value + val;
  console.log("Aumentar potencia: " + newPower);
}
function downPower() {
  let newPower = power.value--;
  power.value--;
  console.log("Baja potencia: " + newPower);
}
</script>

<style lang="scss" scoped></style>
