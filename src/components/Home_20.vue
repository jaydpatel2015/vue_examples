<template>
    <div>
        <h1>Teleport components</h1>
        <div>
            <teleport to='#footer'>
                <Footer />
            </teleport>
        </div>
    </div>
</template>

<script>
import Footer from './Footer.vue';
export default {
    name:"Home",
    components:{
        Footer
    }
}
</script>
<style scoped>
    h1{
        color:#fd9933
    }
    
</style>
