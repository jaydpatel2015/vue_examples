<template>
    <div>
        <h1>Multiple Slots Demo</h1>
        <div class="box">
            <Child>
                <template v-slot:header>
                    <img src="../assets/t-shirt.jpg" alt="">
                    <h1>T-Shirt</h1>
                </template>
                <template v-slot:main>
                    <h1>INR 799</h1>
                </template>
                <template v-slot:footer>
                    <button>Buy Now</button>
                </template>
            </Child>
            <Child>
                <template v-slot:header>
                    <img src="../assets/t-shirt_2.jpg" alt="">
                    <h1>T-Shirt</h1>
                </template>
                <template v-slot:main>
                    <h1>INR 599</h1>
                </template>
                <template v-slot:footer>
                    <button>Buy Now</button>
                </template>
            </Child>
            <Child>
                <template v-slot:header>
                    <img src="../assets/t-shirt_3.jpg" alt="">
                    <h1>T-Shirt</h1>
                </template>
                <template v-slot:main>
                    <h1>INR 699</h1>
                </template>
                <template v-slot:footer>
                    <button>Buy Now</button>
                </template>
            </Child>
        </div>
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
    img{
        height: 200px;
        width:200px;
    }
    .box{
        display: flex;
    }
</style>