<template>
  <img width="128" height="128" :src="avatar" :alt="descricao">
</template>

<script>
  export default {
    name: 'Picture',
    data() {
      return {
        avatar: '/img/avatar.jpg',
        descricao: 'José Víctor'
      }
    }
  }
</script>