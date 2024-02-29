<template>
  <div class="row gx-4 gx-lg-5">
    <div class="col-md-4 mb-5" v-for="pais in paises" :key="pais.name">
        <Card :pais="pais" />
    </div>
  </div>
</template>

<script>
import Card from './Card.vue';
import { computed, onMounted } from 'vue';
import {useStore} from 'vuex';

export default {
    name: 'CardList',
    components: {
        Card
    },
    setup(){
        const store = useStore()
        const paises = computed(() => {
            return store.getters.topPaisesPoblacion
        })

        onMounted(async() => {
            await store.dispatch('getPaises')
            await store.dispatch('filtrarRegion', 'Europe')
        })
        return {paises}
    }
}
</script>

<style>

</style>