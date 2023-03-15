<template>
  <div>
    <custom_header v-bind:isLogged="true" />
    <primeiro_componente />
    <life_cycle />
    <people />
  </div>
</template>

<script>
import custom_header from "./components/custom_header.vue";
import life_cycle from "./components/life_cycle.vue";
import people from "./components/people.vue";
import primeiro_componente from "./components/primeiro_componente.vue";

export default {
  name: "App",
  components: {
    custom_header,
    life_cycle,
    people,
    primeiro_componente,
  },
};
</script>

<style>
body {
  background-color: black;
  color: white;
}
a {
  color: greenyellow;
}
</style>