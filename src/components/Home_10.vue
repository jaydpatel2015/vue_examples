<template>
    <div>
        <h1>Props Example</h1>   
        <Student :sname="name"/>
        <Teacher :tname="name" />
    </div>
</template>

<script>
import Student from './Student.vue';
import Teacher from './Teacher.vue';

    export default {
        name:'Home',
        data(){
            return{
                name:"Jay"
            }
        },
        components:{
            Student,
            Teacher,
        }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
