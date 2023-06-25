<template>
  <div>
    <h1>Verificación CAR Composition</h1>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <button @click="testPower">Aumentar</button>
    <button @click="downPowerFn">Disminuir</button>
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
  emits: ["downPower"],
  setup(props, context) {
    console.log('Props: ', props);
    const brand = "Audi";
    const model = "A4";
    const testPower = () => {
      props.upPower();
    }
    const downPowerFn = () => {
      context.emit("downPower");
    }
    return {
      brand,
      model,
      testPower,
      downPowerFn
    };
  },
};
</script>

<style lang="scss" scoped></style>
