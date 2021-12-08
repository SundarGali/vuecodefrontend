<template>
<div>
    <h1> {{Projectname}} </h1>
    
    <h4> {{DonebyName}} </h4>
</div>
</template>

<script>

export default{
    name: 'Header',
    props:{
        Projectname: String,
        DonebyName:String
    }
}

</script>

<style scoped>

div{
    text-align: center;
}

</style>