<template>
  <div>
    <button @click="first($event), second($event), third()">
      Ativar Eventos
    </button>
    <p>{{ multiple_events }}</p>
  </div>
</template>

<script >
export default {
  name: "Multiple Events",
  data() {
    return {
      multiple_events: "",
    };
  },
  methods: {
    first(event) {
      this.multiple_events = "Primeiro Evento Ativado!";
    },
    second(event) {
      setTimeout(() => {
        this.multiple_events = "Primeiro e Segundo Evento Ativado!";
      }, 500);
    },
    third() {
      setTimeout(() => {
        this.multiple_events = "/clear";
      }, 1500);
      setTimeout(() => {
        this.multiple_events = "....";
      }, 2000);
      setTimeout(() => {
        this.multiple_events = "...";
      }, 2250);
      setTimeout(() => {
        this.multiple_events = "..";
      }, 2500);
      setTimeout(() => {
        this.multiple_events = ".";
      }, 2750);
      setTimeout(() => {
        this.multiple_events = "";
      }, 3000);
    },
  },
};
</script>

<style scoped>
div {
  margin: 100px;
}
</style>