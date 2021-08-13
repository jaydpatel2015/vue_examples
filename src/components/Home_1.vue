<template>
    <div>
        <h1>Home Component </h1>    
        <h2>{{data}}</h2>  
        <h2>Email: {{email}}</h2>  
        <h2>mobile: {{mobile}}</h2>  
        <h2>Get Name: {{getName()}}</h2>  
        <h2>Method Name: {{newMethodName("Jay")}}</h2>  
        <h2>Get Details: {{getDetails().name}}</h2>  
        <h2>Get Details: {{getDetails().email}}</h2>  
    </div>
</template>

<script>
export default {
    name:'Home',
    props:{
        data: String,
    },
    data(){
        return {
            email:"jay@gmail.com",
            mobile:121564,
            getName:function(){
                return "Jay Patel"
            },
        }
    },
    methods:{
        newMethodName(name){
            return name;
        },
        getDetails(){
            return{
                name:"Roman Reigns",
                email:"roman@gmail.com"
            }
        }
    }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
