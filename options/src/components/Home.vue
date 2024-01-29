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
        //Aqui uso desestructuracion para elegir lo que quiero
        //pero el objeto es context y accedo a la variable que necesito
        //aunque context puede tener cualquier nombres siempre es
        //el segundo argumento
        setup(props, {expose}) {

            console.log(expose);

            //toRefs es para hacer todo reactivo pero al final
            //de este codigo hay un ejemplo para una sola propiedad
            const { firstName, lastName } = toRefs(props);

            const fullName = computed(() => {
                return `${firstName.value} ${lastName.value}`;
            });

            //Esta es la manera de permitir que
            //accedan a variables del setupt desde fuera
            expose({
                fullName,
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