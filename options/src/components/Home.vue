<template>
    <div> {{ obj.counter }} </div>
</template>

<script>

    // eslint-disable-next-line no-unused-vars
    import { ref, reactive } from 'vue';

    export default {
        setup() {
            //ref hace que la variables sea reactiva y es para
            //las variables primitivas y se coge el valor
            //usando .value
            //reactive se usa para los objetos y hace que sea
            //reactivo cada propiedad y eso no lo hace reactive
            const obj = reactive({ counter: 0});

            setInterval(() => obj.counter++, 1000);
            
            return {
                obj
            }
        }
    };
</script>