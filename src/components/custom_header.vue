<template>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projetos</a></li>
    <li><a href="#">Contato</a></li>
    <li v-if="isLogged">
      <a href="#">Meu Perfil</a>
    </li>
    <li v-else>
      <a href="#">Cadastre-se</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "custom_header",
  props: ["isLogged"],
};
</script>

<style scoped>
ul {
  background-color: whitesmoke;
  display: flex;
  list-style: none;
  height: 50px;
  align-items: center;
}

li {
  margin-right: 10px;
}

a {
  color: black;
  text-decoration: none;
  font-size: 16px;
  transition: 1s;
}

a:hover {
  font-size: 20px;
  color: turquoise;
}
</style>