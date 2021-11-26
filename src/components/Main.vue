<template>
 
    <main> 
      <div class="jumbotron">
        <img src="../assets/img/jumbotron.jpg" alt="">
      </div>
        
      <div class="series-container">
        <div class="wrapper container">
           <ItemSeries
           v-for="(serie,index) in listSeries" :key="index"
           :serieImage="serie.thumb"
           :serieName="serie.series"
           />
        </div>
      </div>
      
    </main>
 
</template>


<script>

import ItemSeries from './ItemSeries'
import listSeries from '../assets/data/listSeries.js'
export default {
   name:'Main',
   components:{
     ItemSeries:ItemSeries,
   },
   data(){
     return{
       listSeries
     }
   }
   }
</script>

<style scoped lang="scss">
@import '../assets/style/mixin.scss';
main{
.jumbotron{
  max-height: 50vh;
  overflow: hidden;
  img{
  width: 100%;
  }
}

 
  .series-container{
 
    background-color:#1c1c1c;
    width: 100%;
     
    .wrapper{
      display: flex;
      flex-wrap:wrap;
      padding:50px 0px ;
     
    }
  }

}
</style>

          
  
  