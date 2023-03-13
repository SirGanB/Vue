<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ name }}, e trabalho como {{ profissao }}.</p>
    <multipleEvents />

    <h2>Botões Independetes</h2>
    <reusable />
    <reusable />
    <reusable />
    <reusable />
    <reusable />
  </div>
</template>

<script>
import reusable from "./reusable.vue";
import multipleEvents from "./multiple_events.vue";

export default {
  name: "primeiro_componente",
  components: {
    multipleEvents,
    reusable,
  },
  data() {
    return {
      name: "GanB",
      profissao: "programador",
    };
    //#app pode ter a func data();
  },
};
</script>