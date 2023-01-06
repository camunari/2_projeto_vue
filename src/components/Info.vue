<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou a procura de novas oportunidades!</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <p>Para acessar o meu portifólio, clique <a v-bind:href="meu_link" target="blank">aqui</a>!</p>
    <ul>
      <li>Javascript</li>
      <li>PHP</li>
      <li>Python</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
    esta_trabalhando: false,
    meu_link: 'https://github.com/camunari'
    }
  },
}
</script>

<style>
</style>