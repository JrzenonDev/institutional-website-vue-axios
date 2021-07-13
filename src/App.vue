<template>
  <div id="app">
    <Header />
    <Home />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Home from './pages/Home.vue';

import './assets/css/globals.css';

export default {
  name: 'App',
  components: {
    Header,
    Home,
  }
}
</script>

<style>

</style>
