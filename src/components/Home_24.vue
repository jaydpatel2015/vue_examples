<template>
    <div>
        <h1>Call API</h1>
        <table class="table">
            <thead>
                <tr>
                    <th>ID</th>
                    <th>First Name</th>
                    <th>Last Name</th>
                    <th>Email</th>
                    <th>Avatar</th>
                </tr>  
            </thead>   
            <tbody v-for="item in list" :key="item">
                <tr>
                    <td>{{item.id}}</td>
                    <td>{{item.first_name}}</td>
                    <td>{{item.last_name}}</td>
                    <td>{{item.email}}</td>
                    <td><img :src="item.avatar" class="img-responsive"></td>
                </tr>
            </tbody>      
        </table>
    </div>
</template>

<script>
import axios from "axios";
export default {
    name:"Home",
    data(){
        return{
            list:[]
        }
    },
    async mounted(){
        let res=await axios.get("https://reqres.in/api/users?page=2");
        this.list=res.data.data;

    }
    
}
</script>

<style scoped>
    h1{
        color:blue;
    }
    .table{
        border:1px solid black;
        
    }
    .table thead tr th{
        border:1px solid black;
        padding:10px;
    }
    .table tbody tr td{
        border:1px solid black;
        padding:10px;
    }
    .table tbody tr td img{
        height: 50px;
        width:50px;
    }
    
</style>


