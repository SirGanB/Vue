<template>
    <div>
        <h2>
            Profile.{{ name }}
        </h2>
        
        <info />
        <custom_form />
    </div>
</template>

<script>
    import info from './info.vue';
    import custom_form from './custom_form/custom_form.vue';

    export default{
        name: 'people',
        components: {
            info,
            custom_form,
        },
        data() {
            return {
                name: 'GanB'
            }
        }
    }
</script>