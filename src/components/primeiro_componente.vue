<template>
    <div>    
        <h1>Olá Vue!</h1>
        <p>Meu nome é {{ name }}, e trabalho como {{ profissao }}.</p>
    </div>
</template>

<script>

    export default {
    name: 'primeiro_componente',
    data() {
        return {
            name: 'GanB', 
            profissao: 'programador',
        }
        //#app pode ter a func data();
    }
 }
</script>