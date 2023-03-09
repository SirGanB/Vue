<template>
    <div>
        <p v-if="isWorking">
            Situação: Empregado.
        </p>
        <p v-else>
            Situação: Buscando por oportunidades.
        </p>
        <p>
            Conheço as seguintes tecnologias:
        </p>
        <ul>
            <li>Dart/Flutter</li>
        </ul>
        <p>
            Estudando Atualmente:
        </p>
        <ul>
            <li>Dart/Flutter</li>
            <li>JavaScript/Vue</li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'info',
        isWorking: false,
    }
</script>