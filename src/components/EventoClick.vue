<template>
  <h1>Verificación objeto click sin setup en script</h1>
  <h2>{{ text }}</h2>
  <button @click="clickInit()">Validar</button>
</template>

<script>
export default {
  name: "EventoClick",
  setup() {
    const text = "Prueba 2";
    methods: {
      clickInit();
      {
        alert("Prueba de click inicial");
      }
    }
  },
};
</script>

<style scoped></style>
