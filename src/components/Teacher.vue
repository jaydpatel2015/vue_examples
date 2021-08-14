<template>
    <div>
       <h1>Teacher Child Component</h1> 
       <h2>Name: {{tname}}</h2>
    </div>
</template>

<script>
export default {
    name:"Teacher",
    props:{
        tname:String
    }   
}
</script>

<style scoped>
    h1{
        color:cadetblue;    
    }
</style>