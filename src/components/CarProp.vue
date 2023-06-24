<template>
  <div>
    <h1>Verificación CAR Composition</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
  </div>
</template>
<script>
import { ref } from "vue";
export default {
  props: {
    power: {
      type: String,
      default: "60",
    },
  },
  setup(props) {
    console.log(props);
    const brand = "Audi";
    const model = "A4";
    return {
      brand,
      model,
    };
  },
};
</script>

<style lang="scss" scoped></style>
