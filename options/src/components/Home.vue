<template>
    <div> {{ fullName }} </div>
    <div>{{ username }}</div>
    <button ref="btn">Click!</button>
</template>

<script setup>
    import { defineExpose, defineProps, ref, computed, toRefs, inject, watch } from 'vue';

    const props = defineProps(
        {
            firstName: String,
            lastName: String,
        }
    );

    const { firstName, lastName } = toRefs(props);

            const fullName = computed(() => {
                return `${firstName.value} ${lastName.value}`;
            });

            const username = inject("username");


            defineExpose({
                fullName,
            });

            const btn = ref(null);

            console.log(btn.value);

            watch(btn, (valor) => {
                console.log(valor);
            });

</script>

<!-- import { ref, toRef } from "vue";

props: {
  firstName: String,
},
setup(props) {
  const firstName = toRef(props, 'firstName');
  const firstName = ref(props.firstName);
} -->