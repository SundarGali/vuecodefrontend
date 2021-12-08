<template>
    <!--div v-if="book.published == false"-->

    <div :class="!coincryp.inmarket ? 'green': 'red' ">

    <h4 id="h44">{{coincryp.name}}</h4>
    <h4> {{coincryp.year}}</h4>
    <h4> Price : {{coincryp.price}}</h4>
    <h4> Status : {{coincryp.inmarket?'Active':'Out of the market' }}</h4>

    
    



    </div>
</template>

<script>

export default{
    name: 'COIN',
    props:{
        coincryp: Object
    }
}
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');
h2{
 font-family: 'Montserrat', sans-serif;
}
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,200;1,500&display=swap');
#h44{
    margin: 0px;
    font-family: 'Montserrat', sans-serif;
    font-size: 20px;
    padding-bottom: 15px;
   


}
h4{
     padding-bottom: 5px;
}
div{
    background-color:burlywood ;
    color: crimson;
    padding: 1em;
    
}

.red{
background-color: beige ;

}


</style>