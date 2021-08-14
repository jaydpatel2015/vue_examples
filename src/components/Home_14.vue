<template>
    <div>
        <h1>Form Modifiers</h1>
        <input type="text" v-model.number="data">
        <h2>Data is: {{typeof(data)}}</h2>
    </div>
</template>

<script>
export default {
    name:"Home",
    data(){
        return{
            data:""
        }
    }
}
</script>

<style scoped>
    h1{
        color:orange
    }
</style>