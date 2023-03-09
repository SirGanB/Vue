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

    <p>Conhecimento nas Linguagens:</p>
    <ul>
      <li v-for="(technology, index) in languages" :key="index">
        {{ technology }}
      </li>
    </ul>
    <p>Conhecimento nos Frameworks:</p>
    <ul>
      <li v-for="technology in frameworks" :key="technology.id">
        {{ technology.language }}
      </li>
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
      //Array de String
      languages: ["Dart", "C#", "JavaScript", "DokaLanguage"],
      //Array de Object
      frameworks: [
        { id: 1, language: "Flutter" },
        { id: 2, language: "Vue.js" },
      ],
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