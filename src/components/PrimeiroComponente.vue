<template>
  <div>
    <h1>Olá Vue.js!</h1>
    <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
  </div>
</template>

<script defer>
  export default {
    name: "PrimeiroComponente",
    data() {
      return {
        nome: "Víctor",
        profissao: "Programador"
      }
    }
  }
</script>