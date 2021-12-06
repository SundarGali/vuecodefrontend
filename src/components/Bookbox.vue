<template>
    
     <div class="bookbox">
         
        <div v-for="book in books" :key="book.id" >
                
                <Book :book="book"/>
        </div>

        

     </div>

</template>

<script>

import Book from "./Book.vue"
export default{

    name: 'Bookbox',
    components: {
        Book
    },
    props: {
        books: Object
    }

}

</script>


<style>

.bookbox{

    background-color: bisque;
    padding: 1em;
    color: gray;
}
</style>