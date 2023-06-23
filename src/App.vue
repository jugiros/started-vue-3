<template>
  <div>
    <h1>Nuestro primer componente vue js</h1>
    <p>Hola mundo</p>
    <car></car>
    <test></test>
  </div>
</template>

<script>
import Car from "@/components/Car.vue";
import test from "@/components/Test.vue";
import Test from "@/components/Test.vue";
export default {
  components: {Test, Car}
};
</script>

<style lang="scss" scoped></style>
