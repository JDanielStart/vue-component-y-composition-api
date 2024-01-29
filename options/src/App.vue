<script setup>

</script>

<template>
  <div>
    <div>{{ text }}</div>
    <div>{{ algo }}</div>
  </div>
</template>

<script>

  //Los mixins se usan en Vue2 pero es recomendable sustituirlos
  //por composition API
  import base from "@/mixins/base";

  export default {
    name: "App",
    mixins: [base],
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
