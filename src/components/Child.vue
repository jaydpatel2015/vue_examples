<template>
    <div>
        <h1>Child component</h1>   
        <h2>{{msg}}</h2>
        <h3>Object passed to child component</h3>
        <h3>Name: {{info.name}}</h3>
        <h3>Email: {{info.email}}</h3>
        <button v-on:click="sendData()">Get Data from Parents</button>
    </div>
</template>

<script>
    export default {
        name:'Child',
        props:{
            msg:String,
            info:Object,
            sendData:Function
        },
}
</script>

<style scoped>
    h1{
        color: blue;
    }
    h2{
        color:red;
    }
</style>
