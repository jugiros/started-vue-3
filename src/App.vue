<template>
  <car-composition></car-composition>
  <h1>Setup</h1>
  <car-composition-setup></car-composition-setup>
</template>
<script>
import {defineComponent} from "vue";
import CarComposition from "@/components/CarComposition.vue";
import CarCompositionSetup from "@/components/CarCompositionSetup.vue";

export default defineComponent({
  components: {CarCompositionSetup, CarComposition}
})
</script>

<style lang="scss" scoped></style>