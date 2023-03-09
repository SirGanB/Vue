<template>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projetos</a></li>
    <li><a href="#">Contato</a></li>
  </ul>
</template>

<script>
export default {
  name: "custom_header",
};
</script>

<style scoped>
ul {
  background-color: white;
  display: flex;
  list-style: none;
  height: 30px;
  width: 200px;
  align-items: center;
}

li {
  margin-right: 10px;
}

a {
  color: darkgrey;
  text-decoration: none;
  transition: 1s;
}

a:hover {
  color: turquoise;
}
</style>