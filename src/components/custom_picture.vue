<template>
    <!-- Sintaxe resumida => vbind:src || :src -->
    <img :src="avatar" :alt="description">
</template>

<script>
    export default {
        name: 'custom_picture',
        data() {
            return {
                avatar: "image/logo.png",
                description: "V-Logo",
            }
        },
    }
</script>