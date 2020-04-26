<template>
  <div>
    <div class="card">
      <h3>Vue 3 Calculator</h3>
      <p>first number</p>
      <input type="text" v-model="n1" name="n1" />
      <p>second number</p>
      <input type="text" v-model="n2" name="n1" />
      <h5>result of the multiplication - {{ multi }}</h5>
      <h5>result of the adding - {{ add }}</h5>
    </div>
  </div>
</template>
<script>
import { reactive, computed, toRefs } from "vue";
function useCalc() {
  let calc = reactive({
    n1: 0,
    n2: 0,
    multi: computed(() => parseInt(calc.n1) * parseInt(calc.n2)),
    add: computed(() => parseInt(calc.n1) + parseInt(calc.n2)),
  });
  return toRefs(calc);
}

export default {
  name: "Calc",
  setup() {
    let { n1, n2, multi, add } = useCalc();

    return {
      n1,
      n2,
      multi,
      add,
    };
  },
};
</script>
