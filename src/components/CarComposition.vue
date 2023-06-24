<template>
  <div>
    <h1>Verificación CAR Composition</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <button @click="upPower(20)">Aumentar</button>
    <button @click="downPower()">Disminuir</button>
  </div>
</template>
<script>
import { ref } from "vue";
export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    let power = ref(40);

    const upPower = (newPower) => {
      power.value = power.value + newPower;
      console.log("Aumentar potencia: " + power.value);
    };
    const downPower = () => {
      power.value--;
      console.log("Baja potencia: " + power);
    };
    return {
      brand,
      model,
      power,
      upPower,
      downPower,
    };
  },
};
</script>

<style lang="scss" scoped></style>
