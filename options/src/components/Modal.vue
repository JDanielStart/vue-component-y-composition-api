<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
        <button @click="toggle">Modal</button>
        <teleport to='body'>
            <div v-show="show" class="modal">
                <h1>Titulo</h1>
                <p>Lorem ipsum dolor sit</p>
                <button @click="toggle">cerrar</button>
            </div>
            </teleport>
    </div>
</template>

<script>
export default {
    data() {
        return {
            show: false
        }
    },
    methods: {
        toggle() {
            this.show = !this.show;
        }
    }
};
</script>