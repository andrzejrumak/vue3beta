<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue 3 beta App" />
    <Calc></Calc>
    <FullName></FullName>
    <Counter></Counter>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import FullName from "./components/FullName.vue";
import Calc from "./components/Calc.vue";
import Counter from "./components/Counter.vue";

export default {
  components: {
    HelloWorld,
    FullName,
    Calc,
    Counter,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
