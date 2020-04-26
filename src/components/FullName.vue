<template>
  <div>
    <h3>Full name</h3>
    <input type="text" v-model="name.fn" name="fn" placeholder="first name" />
    <input type="text" v-model="name.sn" name="sn" placeholder="last name" />
    <h6>{{name.fulln}}</h6>
  </div>
</template>
<script>
import { reactive, computed } from "vue";
export default {
  name: "FullName",

  setup() {
    let name = reactive({
      fn: "",
      sn: "",
      fulln: computed(() => name.fn + " " + name.sn)
    });
    return {
      name
    };
  }
};
</script>