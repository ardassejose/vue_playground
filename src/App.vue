<template>
  <div>
    <Header :isLogged="true" />
    <PrimeiroComponente />
    <p>O dado de app é: {{ teste }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponente.vue';
  import LifeCycle from './components/LifeCycle.vue';
  import Pessoa from './components/Pessoa.vue';
  import Header from './components/Header.vue';

  export default {
    name: "App",
    components: {
      Header,
      PrimeiroComponente,
      LifeCycle,
      Pessoa
    }, 
    data() {
      return {
        teste: "testando"
      }
    }
  }
</script>

<style>
  body {
    background: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000;
    padding: 10px;
  }
</style>