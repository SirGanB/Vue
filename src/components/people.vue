<template>
  <div>
    <custom_picture />

    <h2>Profile.{{ name }}</h2>

    <info :email="email" v-bind:isWorking="isWorking" />
    <custom_form />
  </div>
</template>

<script>
import custom_form from "./custom_form/custom_form.vue";
import info from "./info.vue";
import custom_picture from "./custom_picture.vue";

export default {
  name: "people",
  components: {
    custom_form,
    info,
    custom_picture,
  },
  data() {
    return {
      name: "GanB",
      email: "ganb.teste@email.com",
      isWorking: false,
    };
  },
};
</script>