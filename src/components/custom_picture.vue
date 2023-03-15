<template>
  <div>
    <!-- Sintaxe resumida => vbind:src || :src -->
    <img :src="avatar" :alt="description" />
    <ChangePicture @change-image="changeImage" />
  </div>
</template>

<script>
import ChangePicture from "./change_picture.vue";
export default {
  name: "custom_picture",
  components: {
    ChangePicture,
  },
  data() {
    return {
      avatar: require("@/assets/p1.png"),
      description: "description",
    };
  },
  methods: {
    changeImage() {
      this.avatar = require("@/assets/p2.png");
    },
  },
};
</script>

<style scoped>
button {
  background: whitesmoke;
}

img {
  height: 200px;
  width: 200px;
}
</style>