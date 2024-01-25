<template>
  <div>
    <p>{{ email }} </p>
    <p v-if="isWorking">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de um trampo</p>
    <p>Utilizo as seguintes tecnologias para Backend:</p>
    <ul>
      <li v-for="(tech, index) in backendTechnology" v-bind:key="index">
        {{ tech }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para Frontend:</p>
    <ul>
      <li v-for="(tech, index) in frontendTechnology" :key="index">
        {{ tech.language }}
      </li>
    </ul>
    <div>
      <button @click="showEmailName">{{ textButton }}</button>
    </div>
    <p v-show="showEmail">Mande uma mensagem para: {{ email }}</p>
    <p class="teste">
      Para acessar meu portfólio
      <a v-bind:href="myLink" target="_blank">clique aqui</a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from "./Picture.vue";

export default {
  name: "Info",
  components: {
    Picture,
  },
  props: {
    email: String
  },
  data() {
    return {
      isWorking: true,
      showEmail: false,
      myLink: "https://www.google.com",
      textButton: "Mostrar e-mail",
      backendTechnology: ["Javascript", "Java", "C#", "MongoDB", "CSS"],
      frontendTechnology: [
        {id: 1, language: "Java"},
        {id: 2, language: "HTML"},
        {id: 3, language: "CSS"},
        {id: 4, language: "Tailwind CSS"},
      ]
    };
  },
  methods: {
    showEmailName() {
      this.showEmail = !this.showEmail;
      if (!this.showEmail) {
        this.textButton = "Mostrar e-mail";
      } else {
        this.textButton = "Esconder e-mail";
      }
    },
  },
};
</script>