<script setup>
  import Modal from "./components/Modal.vue"
</script>

<template>
  <div>
    <Modal/>
  </div>
</template>

<script>
  export default {
    name: "App",
    components: { Modal },
    data() {
      return {
        show: false,
      }
    }
  }
</script>

<style scoped>

</style>
