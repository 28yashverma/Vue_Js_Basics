<template>
    <h2>
        <ComponentC/>
    </h2>
</template>

<script>
import ComponentC from './ComponentC.vue';

    export default{
        name:"ComponentB",
        components: {
            ComponentC,
        }
    }
</script>

<style scoped>

</style>