<template>
    <div>
        <h1>Single & Multiple Slots Demo</h1>
        <Child>
            <h1>Welcome to Vue Js</h1>
            <h1><a href="https://v3.vuejs.org/">Official Docs</a> can be found here.</h1>
            <img src="../assets/v3_pic.png" alt="">
        </Child>
    </div>
</template>

<script>
import Child from './Child.vue'
export default {
    name:"Home",
    components:{
        Child
    }
}
</script>

<style scoped>
    h1{
        color:orange
    }
</style>