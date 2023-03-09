<template>
  <div>
    <button @click="showEmail">{{ button_text }}</button>

    <p v-if="isPublic">E-Mail: ganb.tads@gmail.com</p>

    <p v-if="isWorking">Situação: Empregado.</p>
    <p v-else>Situação: Buscando por oportunidades.</p>

    <p>
      Para mais informações:
      <a v-bind:href="linkedin" target="_blank">Linkedin</a>
    </p>

    <p>Conheço as seguintes tecnologias:</p>
    <ul>
      <li>Dart/Flutter</li>
    </ul>
    <p>Estudando Atualmente:</p>
    <ul>
      <li>Dart/Flutter</li>
      <li>JavaScript/Vue</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "info",
  data() {
    return {
      isPublic: false,
      isWorking: true,
      linkedin:
        "https://www.linkedin.com/in/gustavo-amorim-novaes-bueno-821b61237/",
      button_text: "Mostrar E-Mail",
    };
  },
  methods: {
    showEmail() {
      this.isPublic = !this.isPublic;

      if (!this.isPublic) {
        this.button_text = "Mostrar E-Mail";
      } else {
        this.button_text = "Esconder E-Mail";
      }
    },
  },
};
</script>