<template>
<div>
    <h1>Computed property</h1>
    <h2>{{getResult}}</h2>
</div>
</template>

<script>
export default {
    name: "Home",
    data(){
        return{
            dollars:100,
            rupeeVal:50,
            discountVal:10
        }
    },
    computed:{
        getResult(){
            return (this.dollars*this.rupeeVal)-this.discountVal;
        }
    }
}
</script>

<style scoped>
h1 {
    color: orange
}
</style>
