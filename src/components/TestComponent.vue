<template>
  <div>

    <button @click="changeMessage">Cliquez moi</button>
  </div>
</template>

<script>
export default {
  name: "TestComponent",
  data() {
    return {
      message: "Salut à tous",
    };
  },
  props: {
    message2: {
      type: String,
      default: "default",
    },
  },
  methods: {
    changeMessage(){
      this.message = "Message modifié !!"
    }
  }
}
</script>
<style scoped>
</style>
