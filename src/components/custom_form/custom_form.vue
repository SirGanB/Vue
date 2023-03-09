<template>
    <div>
        <h2>Formulário Custumizado:</h2>        
        <form action="">
            <div>
                <input_text />
            </div>

            <div>
                <input_text />
            </div>

            <div>
                <submit />
            </div>
        </form>
    </div>
</template>

<script>
    import input_text from './input_text.vue';
    import submit from './submit.vue';

    export default {
        name: 'custom_form',
        components: {
            input_text,
            submit,
        }
    }
</script>