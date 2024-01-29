<template>
    <div> {{ obj.counter }} </div>
</template>

<script>

    // eslint-disable-next-line no-unused-vars
    import { ref, reactive } from 'vue';

    export default {
        setup() {
            //ref hace que la variables sea reactiva
            const obj = reactive({ counter: 0});

            setInterval(() => obj.counter++, 1000);
            
            return {
                obj
            }
        }
    };
</script>