<template>
    <div>
        <h2>Child Component</h2>        
        <button v-on:click="name(uname)">Send user Name</button>
    </div>
</template>

<script>
export default {
    name:"User",
    props:{
        name:Function
    },
    data(){
        return{
            uname:"Rock",
        }
    }

}
</script>

<style scoped>
    h2{
        color:red;
    }
</style>
