<template>
  <div>
    <button @click="primeiro(txt1, $event), segundo(txt2,$event), terceiro($event)">Ativar múltiplos eventos</button>
    <p>{{ multiplosEventos }}</p>
  </div>
</template>

<script>
export default {
  name: "MultiplosEventos",
  data() {
    return {
      multiplosEventos: "",
      txt1: "Primeiro text",
      txt2: "Segundo text"
    }
  },
  methods: {
    primeiro(txt, e) {
      this.multiplosEventos = txt
    },
    segundo(txt, e) {
      setTimeout(() => this.multiplosEventos = txt, 500)
    },
    terceiro() {
      setTimeout(() => this.multiplosEventos = "", 1500)
    }
  }
}
</script>

<style scoped>
  div {
    margin: 100px;
  }
</style>