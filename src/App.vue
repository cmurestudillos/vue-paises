<template>
  <Navbar />
  <div class="container px-4 px-lg-5">
    <Buscador />
    <CardList />
  </div>
  <Footer />
</template>

<script>
import Navbar from './components/Navbar.vue';
import CardList from './components/CardList.vue';
import Buscador from './components/Buscador.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    CardList,
    Buscador,
    Footer
  }
}
</script>
