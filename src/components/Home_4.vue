<template>
    <div>
        <h1>Conditional Rendering</h1>   
        <h2 v-if="show">If-Else Condition</h2>
        <h2 v-else>Else Condition</h2>
        <br>
        <br>
        <button v-on:click="show=!show">Toggle if-else</button>
    </div>
</template>

<script>
    export default {
        name:'Home',
        data(){
            return{
                show:true
            }
        }
    }
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
