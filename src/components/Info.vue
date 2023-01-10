<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou a procura de novas oportunidades!</p>
    <div>
      <button @click="showEmail">{{textoBotao}}</button>
    </div>
    <p v-show="mostrar_email" >Mande uma mensagem para: {{ email }}</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <p>Para acessar o meu portifólio, clique <a v-bind:href="meu_link" target="blank">aqui</a>!</p> <!--o v-binde é um recurso vue que faz o link ir realmente para o endereço dele no html-->
    <Picture />
    <ul>
      <li>Javascript</li>
      <li>PHP</li>
      <li>Python</li>
    </ul>
  </div>
</template>

<script>
import Picture from './Picture.vue';
export default {
  name: 'Info',
  components: {
    Picture
  },
  data() {
    return {
    esta_trabalhando: false,
    mostrar_email: false,
    meu_link: 'https://github.com/camunari',
    email: 'carla.munari95@gmail.com',
    textoBotao: 'Mostrar e-mail'
    }
  },
  methods: {
    showEmail() { //ISSO ACONTECE AO CLICAR NO BOTAO 
      this.mostrar_email = !this.mostrar_email; //se houver click, o mostrar_email verdadeiro exibe e volta pra condicao falsa. segue as condições:
      if (!this.mostrar_email) { //se o mostrar email for falso, ele exibe o email
        this.textoBotao = 'Exibir o E-mail'
      } else { // 
        this.textoBotao = 'Ocultar E-mail'; // se nao, ele oculta o email
      }
    }
  }
}
</script>

<style>
</style>