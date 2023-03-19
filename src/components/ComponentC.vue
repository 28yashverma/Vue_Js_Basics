<template>
    <h2>
        Component C : {{ username }}
    </h2>
</template>

<script>
    export default{
        name:"ComponentC",
        inject: ['username']
    }
</script>

<style scoped>

</style>