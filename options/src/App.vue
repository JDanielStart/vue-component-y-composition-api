<script setup>
  import Menus from "./components/Menus.vue";
</script>

<template>
  <button @click="show = !show">Menu</button>
  <transition name="fade">
    <Menus v-show="show"/>
  </transition>
</template>

<script>
  export default {
    name: "App",
    components: {},
    data() {
      return {
        show: false,
      }
    }
  }
</script>

<style scoped>

  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }

  .fade-leave-active,
  .fade-enter-active {
    transition: opacity 0.5s ease;
  }
</style>
