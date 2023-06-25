<template>
  <!--  <car-composition></car-composition>-->
  <!--  <h1>Setup</h1>-->
  <!--  <car-composition-setup></car-composition-setup>-->
  <car-prop :power="power" :up-power="upPower"></car-prop>
  <h2>Setup</h2>
  <car-prop-setup :power="power" :up-power="upPower"></car-prop-setup>
</template>
<script>
import {ref} from "vue";
import { defineComponent } from "vue";
import CarPadre from "@/components/CarProp.vue";
import CarPropSetup from "@/components/CarPropSetup.vue";
import CarProp from "@/components/CarProp.vue";
// import CarComposition from "@/components/CarComposition.vue";
// import CarCompositionSetup from "@/components/CarCompositionSetup.vue";

export default defineComponent({
  components: { CarProp, CarPropSetup },
  // components: {CarCompositionSetup, CarComposition}
  setup() {
    let power = ref(30);
    const upPower = () => {
      power.value++
      console.log('Aumentar potencia');
    }
    return {
      power,
      upPower
    };
  },
});
</script>

<style lang="scss" scoped></style>
