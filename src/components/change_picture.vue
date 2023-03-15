<template>
  <div>
    <button @click="$emit('changeImage')">Trocar Imagem</button>
  </div>
</template>

<script>
export default {
  name: "change_image",
  emits: ["changeImage"],
};
</script>
