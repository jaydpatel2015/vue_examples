<template>
    <div>
        <h1>Home Component </h1>    
        <button v-on:click="test('Button 1 Clicked')">Button 1</button>
        <button v-on:dblclick="test('Button dbl Clicked')">Button 2</button>
        <br>
        <br>
        <button v-on:click="getitemCount()">Click to count</button>
        <h2>{{count}}</h2>
    </div>
</template>

<script>
export default {
    name:'Home',
    data(){
        return{
            count:0
        }
    },
    methods:{
        test(data){
            alert (data)
        },
        getitemCount(){
            this.count = this.count + 1
        }
    }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
