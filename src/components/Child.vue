<template>
    <div>
        <div class="cart">
            <header>
                <slot name="header"></slot>
            </header>
            <main>
                <slot name="main"></slot>
            </main>
            <footer>
                <slot name="footer"></slot>
            </footer>
        </div>
    </div>
</template>

<script>
export default {
    name:"Child",
    props:{
        data:String
    }
}
</script>

<style scoped>
    .cart{
        margin-top: 10px;
        margin-right: 10px;
        width: 200px;
        border: 1px solid black;
        text-align: center;
        padding: 10px;
    }
</style>