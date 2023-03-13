<template>
  <div>
    <button @click="active">Red Button</button>
    <span v-show="isActive"> Katsu 喝</span>
  </div>
</template>

<script>
export default {
  name: "reusable",
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    active() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
button {
  background: darkred;
  border-color: white;
  color: white;
}
</style>