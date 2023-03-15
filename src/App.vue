<script>
import Calculadora from './components/Calculadora.vue';

export default {
  name: 'App',
  components: {
    Calculadora,
  },
};
</script>

<template>
  <div class="container">
    <header class="p-3 mb-4 mt-4 bg-dark text-center text-white rounded-3">
      <h1>Calculadora Aritmética</h1>
    </header>
    <div id="app">
      <Calculadora />
    </div>
  </div>
</template>