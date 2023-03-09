<template>
    <h1>
        {{ name }}
    </h1>
</template>

<script>
    export default {
        name: 'life_cycle',
        created() {
            this.name = 'created()'
                setTimeout(() => {
                    this.name = 'Life Cycle: created()'
                }, 1000);
        },
        data() {
            return {
                name: 'Life Cycle',
            }
        },
        mounted() {
            this.name = 'mounted()'
                setTimeout(() => {
                    this.name = 'Life Cycle: mounted()'
                }, 2000);
        },
    }
</script>