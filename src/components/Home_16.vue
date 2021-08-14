<template>
<div>
    <h1>Watchera property</h1>
    <h2>{{count}}</h2>
    <button v-on:click="count=count+1"> + </button>
    <button v-on:click="count=count-1"> - </button>
</div>
</template>

<script>
export default {
    name: "Home",
    data(){
        return{
            count:0
        }
    },
    watch:{
        count(val,prev){
            if(val>5 && val>prev || val<0){
                this.count=0  
            }
        }
    }
}
</script>

<style scoped>
h1 {
    color: orange
}
</style>
