<template>
  <div>
    <h1>Nuestro primer componente vue js</h1>
    <p>Hola mundo</p>
    <car></car>
    <p>{{ marca }}</p>
    <p v-for="(val, index) in arrVal" :key="index">{{ index }}: {{ val }}</p>
    <ul>
      <li v-for="(val, index) in arrVal" :key="index">
        {{index}}: {{val}}
      </li>
    </ul>
  </div>
</template>
<script setup>
import Car from "@/components/Car.vue";
const marca = "Chevrolet";
const arrVal = ["uno", "dos", "tres", "uno"];
</script>

<style lang="scss" scoped></style>
