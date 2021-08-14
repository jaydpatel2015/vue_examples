<template>
    <div>
        <h1>Class Binding</h1>   
        <h2 :class="applyStyle">home component</h2>        
        <button v-on:click="colorfull=!colorfull">Toggle Background Color</button>
    </div>
</template>

<script>
export default {
    name:'Home',
    data(){
        return{
            colorfull:true
        }
    },
    computed:{
        applyStyle(){
            return{
                green:this.colorfull,
                err:true,
                other:true,
            }
        }
    }
}
</script>

<style scoped>
    h1{
        color: #fd8700;
    }
    .green{
        background-color: lightgreen;
        width: 4    00px;
    }
    .err{
        color:red
    }
    .other{
        font-size: 40px;
    }
</style>
