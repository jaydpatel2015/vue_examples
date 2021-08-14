<template>
    <div>
        <h1>Ref</h1>
        <input type="text" ref="input"/>
        <button v-on:click="getData">Click me</button>
    </div>
</template>

<script>

export default {
    name:"Home",
    methods:{
        getData(){
            this.$refs.input.focus();
            let boxVal=this.$refs.input.value;
            console.log(boxVal)    
        }
    }
}
</script>

<style scoped>
    h1{
        color:orange;
    }
    h2{
        color:blue;
    }
</style>

