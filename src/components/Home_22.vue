<template>
    <div>
        <h1>Life Cycle Method Demo</h1>
        <h2>beforeCreate & Created Example</h2>
        <h2>beforeMount & Mounted Example</h2>
        <h2>{{name}}</h2>
    </div>
</template>

<script>

export default {
    name:"Home",
    data(){
        return{
            name:"Jay"
        }
    },
    beforeCreate(){
        console.log("before create called");
    },
    created(){
        console.log("Created called");   
    },
    beforeMount(){
        console.log("before Mounted" ,this.$el)
    },
    mounted(){
        console.log("Mounted",this.$el)
    }


}
</script>

<style scoped>
    h1{
        color:#fd8700
    }
    h2{
        color:#5cd1e6
    }
</style>