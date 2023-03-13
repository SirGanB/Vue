<template>
  <div>
    <h2>Formulário Custumizado:</h2>
    <form action="" @submit="sendForm($event)">
      <div>
        <input type="text" v-model="name" />
      </div>

      <div>
        <input type="text" v-model="email" />
      </div>

      <div>
        <submit />
      </div>
    </form>
  </div>
</template>

<script>
import submit from "./submit.vue";

export default {
  name: "custom_form",
  components: {
    submit,
  },
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    sendForm(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log("O nome é: " + name);
      console.log("O e-mail é: " + email);

      console.log("Formulário Enviado!");

      //Ajax
      //Inserir no banco de dados
    },
  },
};
</script>