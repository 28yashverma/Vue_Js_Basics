<template>
    <h2>
        <ComponentB/>
    </h2>
</template>

<script>
import ComponentB from './ComponentB.vue';
    export default{
        name:"ComponentA",
        components: {
            ComponentB,
        }
    }
</script>

<style scoped>

</style>