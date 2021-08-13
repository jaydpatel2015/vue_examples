<template>
    <div>
        <h1> Two Way Binding </h1>    
        <input type="text" v-model="count">
        <h1>{{count}}</h1>


        <h1> Get input field value </h1>    
        <input type="text" placeholder="Enter Name" v-model="email">
        <br>
        <br>
        <input type="password" placeholder="Enter Password" v-model="password">
        <br>
        <br>
        <h1>List</h1>
        <input type="checkbox" value='java' id='java' v-model="technology">
        <label for="java">Java</label>
        <br>
        <br>
        <input type="checkbox" value='php' id='php' v-model="technology">
        <label for="php">PHP</label>
        <br>
        <br>
        <input type="checkbox" value='javascript' id='javascript' v-model="technology">
        <label for="javascript">Javascript</label>
        <br>
        <br>
        <h1>Experience TechStack : {{technology}}</h1>

        <h1>Gender</h1>
        <input type="radio" value='male' name='gender' id='male' v-model="gender">
        <label for="male">Male</label>
        <input type="radio" value='female' name='gender' id='female' v-model="gender">
        <label for="female">Female</label>
        <br>
        <br>
        <h1>Selected Gender : {{gender}}</h1>
        <button v-on:click="getData()">Click me</button>

    </div>
</template>

<script>
export default {
    name:'Home',
    data(){
        return{
            count:10,
            email:null,
            password:null,
            technology:[],
            gender:[]
        }
    },
    methods:{
        getData(){
            console.warn('Values are: ',this.email,this.password)
        }
    }
    
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
</style>
