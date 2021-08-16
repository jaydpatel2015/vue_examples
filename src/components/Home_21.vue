<template>
    <div>
        <h1>Life Cycle Method Demo</h1>
        <h2>beforeCreated & Created Example</h2>
        <h3>after created: {{name}}</h3>
    </div>
</template>

<script>

export default {
    name:"Home",
    data(){
        return{
            name:"jay"
        }
    },
    beforeCreate(){
        console.log("before Create is called")
    },
    created(){
        console.log("Now Create is called")
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