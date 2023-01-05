<template>
  <div>
    <h1>Primeiro Componente</h1>
    <p>Meu nome é {{ nome }}</p>
  </div>
</template>

<script>
export default {
  name: 'PrimeiroComponente',
  data() {
    return {
      nome: 'Carla',
    };
  },
};
</script>

<style>
</style>