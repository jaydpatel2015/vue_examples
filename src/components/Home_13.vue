<template>
    <div>
        <ul>
            <li v-for="item in error" v-bind:key="item">
                <h4>{{item}} is either missing or not valid</h4>
            </li>
        </ul>
        <h1>Form</h1>
        <br>
        <label for="email">Email</label>&nbsp;
        <input type="email" name="email" id="email" placeholder="Enter Email" v-model="form.email" />
        <br>
        <br>
        <label for="pass">Password</label>&nbsp;
        <input type="password" name="password" id="pass" placeholder="Enter Password" v-model="form.password" />
        <br>
        <br>
        <label for="country">Country</label>&nbsp;
        <select name="" id="country" v-model="form.country">
            <option value="">Select your country</option>
            <option value="India">India</option>
            <option value="Canada">Canada</option>
            <option value="UAE">UAE</option>
        </select>
        <br>
        <br>
        <label for="technology">Technology</label>&nbsp;
        <br>
        <br>
        <input type="checkbox" value="Java" id="java" v-model="form.technology">&nbsp;<label for="java">Java</label>
        <input type="checkbox" value="PHP" id="php" v-model="form.technology">&nbsp;<label for="php">PHP</label>
        <input type="checkbox" value="Python" id="python" v-model="form.technology">&nbsp;<label for="python">Python</label>
        <br>
        <br>
        <label for="">Gender</label>&nbsp;
        <br>
        <br>
        <input type="radio" name='gender' value="Male" id="male" v-model="form.gender">&nbsp;<label for="male">Male</label>
        <input type="radio" name='gender' value="Female" id="female" v-model="form.gender">&nbsp;<label for="female">Female</label>
        <br>
        <br>
        <button v-on:click="login" type="button">Submit</button>
            
        <h1>{{form}}</h1>

    </div>
</template>

<script>

export default {
    name:"Home",
    data(){
        return{
            form:{
                email:'',
                password:'',
                country:'',
                technology:[],
                gender:'',
            },
            error:[],
        }
    },
    methods:{
        login(){
            this.error = [];
            for (const item in this.form){
                if(this.form[item] == "" || this.form[item].length == 0){
                        this.error.push(item)
                }
            }   
            if(this.error.length === 0){
                alert("data has been submitted successfully");
            }
            console.log(this.form,this.error);
        }
    }
}
</script>

<style scoped>
    h1{
        color:orange;
    }
    
</style>

