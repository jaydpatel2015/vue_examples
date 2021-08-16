<template>
    <div>
        <h1>Life Cycle Method Demo</h1>
        <h2>beforeCreate & Created Example</h2>
        <h2>beforeMount & Mounted Example</h2>
        <h2>{{name}}</h2>
        <h2>beforeUpdate & Updated Example</h2>
        <h2 ref="count">{{counter}}</h2>
        <button v-on:click="counter=counter+1">Update Count</button>
        <h2>beforeUnmounted & unmounted Example</h2>
        <button v-on:click="show=!show">Click for Toggle</button>
        <User v-if="show" />
    </div>
</template>

<script>
import User from './User.vue';
export default {
    name:"Home",
    components:{
        User
    },
    data(){
        return{
            name:"Jay",
            counter:0,
            show:true
        }
    },
    beforeCreate(){
        console.log("before create called");
    },
    created(){
        console.log("Created called");   
    },
    beforeMount(){
        console.log("before Mounted",this.$el)
    },
    mounted(){
        console.log("Mounted",this.$el)
    },
    beforeUpdate(){
        console.log("before Update",this.$refs['count'].textContent);
    },
    updated(){
        console.log("Updated",this.counter);
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