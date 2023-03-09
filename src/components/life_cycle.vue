<template>
  <h1>
    {{ name }}
  </h1>
</template>

<script>
export default {
  name: "life_cycle",
  data() {
    return {
      name: "Life Cycle State",
    };
  },
  created() {
    setTimeout(() => {
      this.name = "Life Cycle: created()";
    }, 1000);
  },
  mounted() {
    setTimeout(() => {
      this.name = "Life Cycle: mounted()";
    }, 2000);
  },
};
</script>