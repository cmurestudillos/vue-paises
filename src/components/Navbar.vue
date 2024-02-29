<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container px-5">
            <img class="navbar-brand" src="/img/logo.png" width="128" height="128" alt="Paises" title="Paises">
            <div class="text-center">
                <h3 class="text-white">Filtrar por Continente</h3>
                <div class="btn-group mb-3">
                    <button class="btn btn-outline-light" @click="filtro('Europe')">EU</button>
                    <button class="btn btn-outline-light" @click="filtro('Americas')">AM</button>
                    <button class="btn btn-outline-light" @click="filtro('Asia')">AS</button>
                    <button class="btn btn-outline-light" @click="filtro('Oceania')">OC</button>
                    <button class="btn btn-outline-light" @click="filtro('Africa')">AF</button>
                    <!-- <button class="btn btn-outline-light" @click="filtro('all')">ALL</button> -->
                </div>
            </div> 
        </div>
    </nav>
</template>

<script>
// Propiedades de Vuex
import { useStore } from 'vuex';

export default {
    name: 'Navbar',
    setup(){
        const store = useStore()
        const filtro = (region) => {
            store.dispatch('filtrarRegion', region)
        }
        return {filtro}
    }
}
</script>