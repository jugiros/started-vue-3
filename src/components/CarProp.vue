<template>
  <div>
    <h1>Verificación CAR Composition</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <button @click="testPower">Aumentar</button>
  </div>
</template>
<script>
import { ref } from "vue";
export default {
  props: {
    power: {
      type: Number,
      default: 60,
    },
    upPower: {
      type: Function,
      default: () => {
        return console.log('Prueba de function');
      }
    },
  },
  setup(props) {
    console.log('Props: ', props);
    const brand = "Audi";
    const model = "A4";
    const testPower = () => {
      props.upPower();
    }
    return {
      brand,
      model,
      testPower
    };
  },
};
</script>

<style lang="scss" scoped></style>
