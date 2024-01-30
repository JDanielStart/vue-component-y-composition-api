<template>
  <Home first-name="Diana" last-name="Martínez" otro="algo"></Home>
</template>

<script>

  import Home from "./components/Home.vue";
  import { provide } from "vue";

  export default {
    name: "App",
    components: {
      Home,
    },
    setup() {
      provide("username", "DianaNerd");
    }
  }
</script>

<style scoped>

</style>
