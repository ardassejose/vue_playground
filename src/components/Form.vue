<template>
  <form
    action=""
    @submit="enviarFormulario($event)"
    style="display: flex; flex-direction: column; max-width: fit-content"
  >
    <div>
      <input type="text" v-model="name" />
    </div>
    <div>
      <input type="text" v-model="email" />
    </div>
    <Submit />
  </form>
</template>

<script>
import InputText from "./form/InputText.vue";
import Submit from "./form/Submit.vue";

export default {
  name: "Form",
  components: {
    InputText,
    Submit,
  },
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    enviarFormulario(e) {

      e.preventDefault();

      const name = this.name;
      const email = this.email;

      window.alert("Form enviado!");
      window.alert(`O nome é ${name} e o email: ${email}`);
    },
  },
};
</script>