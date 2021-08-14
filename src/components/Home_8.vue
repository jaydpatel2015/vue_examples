<template>
    <div>
        <h1>HTML Binding</h1>   
        <h2>{{text}}</h2>
        <div v-html="tag"></div>
        <div v-html="tag2"></div>
    </div>
</template>

<script>
export default {
    name:'Home',
    data(){
        return{
            text:"simple text",
            tag:"<h1>Tag-1: Text with HTML Binding</h1>",
            tag2:"<h2>Tag-2: Another Text with HTML Binding</h2>"
        }
    }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
