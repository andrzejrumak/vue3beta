<template>
  <div>
    <div class="card">
      <h3>Vue 3 Calculator</h3>
      <p>first number</p>
      <input type="text" v-model="calc.n1" name="n1" />
      <p>second number</p>
      <input type="text" v-model="calc.n2" name="n1" />
      <h5>result of the multiplication - {{ calc.multi }}</h5>
      <h5>result of the adding - {{ calc.add }}</h5>
    </div>
  </div>
</template>
<script>
import { reactive, computed } from "vue";
export default {
  name: "Calc",
  setup() {
    let calc = reactive({
      n1: 0,
      n2: 0,
      multi: computed(() => parseInt(calc.n1) * parseInt(calc.n2)),
      add: computed(() => parseInt(calc.n1) + parseInt(calc.n2)),
    });

    return {
      calc,
    };
  },
};
</script>
