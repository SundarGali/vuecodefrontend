<template>
    <!--div v-if="book.published == false"-->

    <div :class="book.published ? 'green': 'red' ">

    <h2>{{book.name}}</h2>
    <h4> {{book.year}}</h4>

    
    



    </div>
</template>

<script>

export default{
    name: 'Book',
    props:{
        book: Object
    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
}

.red{
background-color: orangered !important;

}


</style>