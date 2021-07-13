<template>
  <div id="app">
    <Header />
    <Home />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Home from './pages/Home.vue';
import Footer from './components/Footer.vue';

import './assets/css/globals.css';

export default {
  name: 'App',
  components: {
    Header,
    Home,
    Footer,
  }
}
</script>

<style>

</style>
