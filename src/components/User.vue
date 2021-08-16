<template>
    <div>
        <h1>User Component</h1>
        <h1 ref="user"></h1>
    </div>
</template>

<script>
export default {
    name:"User",
    beforeUnmount()
    {
        console.log("before unmount",this.$refs['user'])
    },
    unmounted(){
        console.log("unmounted",this.$refs['user']);
    }
}
</script>

<style scoped>
    h1{
        color:blue
    }
</style>