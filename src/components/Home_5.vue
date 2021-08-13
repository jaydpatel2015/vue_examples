<template>
    <div>
        <h1>Loops</h1>   
        <h2 v-for='item in technology' :key="item">{{item}}</h2>
        <hr>
        <h2 v-for='item in user' :key="item">Name: {{item.name}} , Email: {{item.email}}</h2>
    </div>
</template>

<script>
    export default {
        name:'Home',
        data(){
            return{
                technology:['java','php','javascript','laravel'],
                user:[
                    {name:"John",email:"john@gmail.com"},
                    {name:"Dwayne",email:"dwayne@gmail.com"},
                    {name:"Edge",email:"edge@gmail.com"},
                ]
        }
    }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
