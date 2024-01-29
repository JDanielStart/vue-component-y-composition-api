<script setup>

</script>

<template>
  <div>
    <div>{{ text }}</div>
  </div>
</template>

<script>
  export default {
    name: "App",
    data() {
      return {
        text: "Hola Vue",
      }
    },
    beforeCreate() {
      console.log("beforeCreate", this.$data, this.$el); //null null
    },
    created() {
      console.log("created", this.$data, this.$el);//!null null
    },
    mounted() {
      console.log("mounted", this.$data, this.$el);//!null !null
    }
  }
</script>

<style scoped>

</style>
