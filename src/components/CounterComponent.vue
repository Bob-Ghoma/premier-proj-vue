<template>
<div>

  <h1> {{ counter }}</h1>
 <!-- <input type="number" :value="counter" @input="updateCounter"> -->
  <input type="number" v-model="counter">
  <div :key="index" class="task" v-for="(task,index) in tasks">
    <h1>{{ task + index }}</h1>
  </div>
  <button @click="addTasks">Ajouter une tâche</button>
</div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";
export default {
  name: "CounterComponent",
  data() {
    return {
      counter: 0,
      tasks: [
          "commander un kebab",
          "finir mon cours de Vue",
          "Essayer de finir Skyrim"
      ]
    }
  },
  props: {
    message: {
      type: String,
      default: "counter",
    }
  },
  methods: {
    addCounter() {
      this.counter = this.counter + 1
    },
    lessCounter() {
      this.counter = this.counter - 1
    },
    updateCounter(event) {
     this.counter = parseInt(event.target.value);
    },
    addTasks(){
      this.tasks.push('New task');
    }
  },
  components : {
    HelloWorld
  }
}
</script>

<style scoped>

</style>
