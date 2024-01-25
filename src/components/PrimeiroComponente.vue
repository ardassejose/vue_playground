<template>
  <div>
    <h1>Olá Vue.js!</h1>
    <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
    <MultiplosEventos />
  </div>
</template>

<script defer>
  import MultiplosEventos from './MultiplosEventos.vue'

  export default {
    name: "PrimeiroComponente",
    components: {
      MultiplosEventos
    },
    data() {
      return {
        nome: "Víctor",
        profissao: "Programador"
      }
    }
  }
</script>