<template>
  <div>
    <h1>Nuestro primer componente vue js</h1>
    <p>Hola mundo</p>
    <car></car>
    <p>{{ marca }}</p>
    <p v-for="(val, index) in arrVal" :key="index">{{ index }}: {{ val }}</p>
    <ul>
      <li v-for="(val, index) in arrVal" :key="index">
        {{ index }}: {{ val }}
      </li>
    </ul>
    <ul>
      <li v-for="(val, index) in powers" :key="index">
        <!-- Para que no se renderice usamos template, el template no renderiza ninguna etiqueta solo lo interno<p>{{ val }}</p>-->
        <template v-if="parseInt(val) > 90">{{ val }}</template>
      </li>
      <br />
      <template v-for="(val, index) in powers" :key="index">
        <li v-if="parseInt(val) > 90">Mayor: {{ val }}</li>
        <li v-else-if="parseInt(val) == 90">Igual: {{ val }}</li>
        <li v-else>Menor: {{ val }}</li>
      </template>
    </ul>
    <evento-click-setup-script></evento-click-setup-script>
    <evento-click></evento-click>
  </div>
</template>
<script setup>
import Car from "@/components/Car.vue";
import EventoClick from "@/components/EventoClickSetup-Script.vue";
import EventoClickSetupScript from "@/components/EventoClickSetup-Script.vue";
const marca = "Chevrolet";
const arrVal = ["uno", "dos", "tres", "uno"];
const powers = ["80", "90", "100", "120"];
</script>

<style lang="scss" scoped></style>
