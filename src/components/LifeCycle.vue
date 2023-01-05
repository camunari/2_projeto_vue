<template> <!--Tag utilizada para dar inicio ao projeto Vue-->
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script> //Tag JS 
export default { 
  name: 'LifeCycle', //Aqui vem o nome do componente
  data() { //Aqui temos uma função data (dados)
    return { //Aqui retornamos dados 
      nome: 'Ainda não sei', //Retorna o dado 'Ainda não sei'
    };
  },
  created() { //Função created(), é uma Life Cycle Hooks, ou seja, da aos usuários a oportunidade de adicionar seu próprio código em estágios específicos
    setTimeout(() => { //Função setTimeout possibilita que o usuário decida em quanto tempo o dado vai ser carregado na página. Por exemplo, poderiamos ter um loading na página aqui dentro do método mounted() ou, gerenciarmos o carregamento dos dados do banco de dados.
      this.nome = 'Carla'; 
    }, 1000);
  },
  mounted() { //Função mounted(), também é uma Life Cycle Hooks, ou seja, da aos usuários a oportunidade de adicionar seu próprio código em estágios específicos. 
    setTimeout(() => { 
      this.nome = 'Kai';
    }, 2000);
  },
};
</script>

<style>
</style>