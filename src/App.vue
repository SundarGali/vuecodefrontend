<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header bookName="Crypto Currency" 
      authorName="Sundar gali" />


    <Coincrypto :coins="coins"  />




  </div>
</template>
<script>




import Header from './components/Header.vue'
import Coincrypto from './components/Coincrypto.vue'



export default {
  name: 'App',
  components: {
    // 2 register the component 
    Header,
    Coincrypto
  },

  data(){
    return {
      coins:[
        {

        }
      ]
    }
  },
  methods: {
    // promises

      async fetchcoins(){
        

        
  
         
         const res= await fetch('https://finalprocrpy.herokuapp.com/api')

         const data= await res.json()
         console.log(data)
         return data
      }

  },

  async created(){
    this.coins = await this.fetchcoins()
  }
}
</script>










<style>



@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@200&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  background-color:turquoise;
  max-width: 500px;
  margin: 10px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.2em solid black;
  padding: 20px;
  border-radius: 10px;
}

div{
  margin-bottom: 0.5em;
}



</style>


