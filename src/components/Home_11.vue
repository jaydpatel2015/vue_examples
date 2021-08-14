<template>
    <div>

        <h1>Pass Data from Child to Parent Component</h1>
        <h2>Parent Component</h2>
        <h2>Name of child User: {{childUser}}</h2>
        <User :name="getName"/>
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
            childUser:""
        }
    },
    methods:{
        getName(name){
            this.childUser=name
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

