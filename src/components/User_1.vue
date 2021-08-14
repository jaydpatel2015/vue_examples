<template>
    <div class="user">
        <h3>{{stuff.name}}</h3>
        <h3>{{stuff.email}}</h3>
        <button v-on:click="sendName(stuff.name)">Name</button>
    </div>
</template>
 
<script>
export default {
    name:"User",
    props:{
        stuff:Object,
        sendName:Function
    }
}
</script>

<style scoped>
.user{
    background-color: beige;
    border-bottom: 1px solid black;
    padding: 10px;
    margin-bottom: 20px;
    width: 200px;
}
</style>