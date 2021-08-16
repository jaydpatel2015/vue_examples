<template>
    <div>
        <h1>Dynamic Compononent</h1>
        
        <button v-on:click="tech='Java'">Load Java</button> <!-- you can write both way 'v-on:click' or '@click' -->
        <button @click="tech='PHP'">Load PHP</button>
        <button @click="tech='Node'">Load Node</button>
        <component :is="tech" />
    </div>
</template>

<script>
import Java from './Java.vue';
import PHP from './PHP.vue';
import Node from './Node.vue';

export default {
    name:"Home",
    components:{
        Java,Node,PHP
    },
    data(){
        return{
            tech:''
        }
    }
}
</script>

<style scoped>
    h1{
        color:#ff9933
    }
</style>