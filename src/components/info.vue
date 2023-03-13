<template>
  <div>
    <button @click="showEmail">{{ buttonText }}</button>

    <p v-if="isPublic">E-Mail: {{ email }}</p>

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
  props: {
    email: String,
    isWorking: Boolean,
  },
  data() {
    return {
      isPublic: false,
      linkedin:
        "https://www.linkedin.com/in/gustavo-amorim-novaes-bueno-821b61237/",
      buttonText: "Mostrar E-Mail",
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
        this.buttonText = "Mostrar E-Mail";
      } else {
        this.buttonText = "Esconder E-Mail";
      }
    },
  },
};
</script>