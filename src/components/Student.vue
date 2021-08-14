<template>
    <div>
        <h1>Student Child Component</h1>
        <h2>Name: {{sname}}</h2>
    </div>
</template>

<script>
export default {
    name:"Student",
    props:{
        sname:String
    }    
}
</script>

<style scoped>
    h1{
        color:blueviolet;    
    }
</style>

