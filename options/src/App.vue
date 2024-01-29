<script setup>

</script>

<template>
  <UserRepositories :user="'Diana'"></UserRepositories>
</template>

<script>

  import UserRepositories from "./components/UserRepositories.vue";

  export default {
    name: "App",
    components: {
      UserRepositories,
    },
  }
</script>

<style scoped>

</style>
