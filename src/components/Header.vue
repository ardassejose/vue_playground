<template>
  <header>
    <ul>
      <li><a href="">Home</a></li>
      <li><a href="">Sobre</a></li>
      <li><a href="">Descrição</a></li>
      <li><a href="">Contato</a></li>
      <li><a href="">Jurídico</a></li>
    </ul>
  </header>
</template>
<script>
export default {
  name: "Header",
};
</script>

<style scoped>
header {
  background-color: #0d1317;
  border-radius: 10px;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
ul {
  padding: 30px;
  display: flex;
  justify-content: space-between;
}

li {
  list-style-type: none;
}

a {
  color: blue;
  text-decoration: none;
}

a:hover {
  color: #ddd;
  text-decoration: underline;
}
</style>