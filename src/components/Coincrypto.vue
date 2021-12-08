<template>
    
     <div class="coinbody">
         
        <div v-for="coincryp in coins" :key="coincryp.id" >
                
                <Coin :coincryp="coincryp"/>
        </div>

        

     </div>

</template>

<script>

import Coin from "./Coin.vue"
export default{

    name: 'Coincoins',
    components: {
        Coin
    },
    props: {
        coins: Object
    }

}

</script>


<style>

.coinbody{

    background-color: turquoise;
   
    padding: 2em;
    color: gray;
}
</style>