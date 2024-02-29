<template>
    <input type="text" placeholder="Ingrese País" class="form-control my-3" v-model="texto" @keyup="procesarInput">
</template>

<script>
// Propiedades vue
import { ref } from 'vue';
// Propiedades Vuex;
import { useStore } from 'vuex';

export default {
    name: 'Buscador',
    setup(){
        const texto = ref('')
        const store = useStore()

        const procesarInput = () => {
            store.dispatch('filtroNombre', texto.value)
        }

        return {texto, procesarInput}
    }
}
</script>
