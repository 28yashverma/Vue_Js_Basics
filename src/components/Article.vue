<template>
    <h2>
        Article component
    </h2>  
    <div>
    <h2>{{ title }}</h2>
    </div>
</template>

<script>
    export default{
        name: "ArticleComponent",
        props: {
            title: {
                type: String,
                required: true,
                default: 'Default value for the title'
            }
        }
    }
</script>

<style scoped>

</style>