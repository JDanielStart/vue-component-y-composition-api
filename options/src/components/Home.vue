<template>
    <div> {{ fullName }} </div>
</template>

<script>
    import { computed, toRefs } from 'vue';

    export default {
        //Sigue siendo obligatorio porque se pasa esto a setup
        props: {
            firstName: String,
            lastName: String,
        },
        setup(props) {

            //toRefs es para hacer todo reactivo pero al final
            //de este codigo hay un ejemplo para una sola propiedad
            const { firstName, lastName } = toRefs(props);

            const fullName = computed(() => {
                return `${firstName.value} ${lastName.value}`;
            });

            return {
                fullName
            };
        }
    };
</script>

<!-- import { ref, toRef } from "vue";

props: {
  firstName: String,
},
setup(props) {
  const firstName = toRef(props, 'firstName');
  const firstName = ref(props.firstName);
} -->