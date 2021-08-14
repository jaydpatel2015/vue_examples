<template>
    <div>
        <h1>Reuse component</h1>   
        <ul>
            <li v-for="item in users" :key="item">
                <User :stuff="item" :sendName="getName" />
            </li>
        </ul>
    </div>
</template>

<script>
import User from './User.vue';

export default {
    name:'Home',
    components:{
        User,
    },
    methods:{
        getName(item){
            alert(item)
        }
    },
    data(){
        return{
            users:[
                {name:"Tony",email:"Tony@gmail.com"},
                {name:"Clark",email:"clark@gmail.com"},
                {name:"Bruce",email:"Bruce@gmail.com"},
                {name:"Steve",email:"Steve@gmail.com"},
            ]
        }
    }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
