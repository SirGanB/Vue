<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ name }}, e trabalho como {{ profissao }}.</p>

    <multiplos_eventos />
  </div>
</template>

<script>
import multiplos_eventos from "./multiplos_eventos.vue";

export default {
  name: "primeiro_componente",
  components: {
    multiplos_eventos,
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