<template>
  <div id="app">
    <CounterComponent/>
   <test-component/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TestComponent from "@/components/TestComponent";
import CounterComponent from "@/components/CounterComponent";

export default {
  name: 'App',
  components: {
    CounterComponent,
    TestComponent,
    HelloWorld
  }
}
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
