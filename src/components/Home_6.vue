<template>
    <div>
        <h1>Parent data to child component</h1>   
        <Child msg="Some data to child component" :info="user" :sendData='getData'/>
    </div>
</template>

<script>
import Child from './Child.vue' ;
export default {
    name:'Home',
    components:{
        Child
    },
    data(){
        return{
            user:{name:"jay Patel",email:"jay@gmail.com"}
        }
    },
    methods: {
        getData(){
            console.log("parent function called")
            alert("parent function called")
        }
    }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
