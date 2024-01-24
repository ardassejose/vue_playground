<template>
  <form action="" style="display: flex; flex-direction: column; max-width: fit-content;">
    <InputText />
    <InputText />
    <Submit />
  </form>
</template>

<script>
import InputText from './form/InputText.vue';
import Submit from './form/Submit.vue';

  export default {
    name: 'Form',
    components: {
      InputText,
      Submit
    }
  }
</script>