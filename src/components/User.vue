<template>
    <div>
        <h3>Peter</h3>
        <h3>Bruce</h3>
        <h3>Clark</h3>
        <h3>{{data}}</h3>
    </div>
</template>
<script>
export default {
    name:"User",
    props:{
        data:String
    }

}
</script>