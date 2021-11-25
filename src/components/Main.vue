<template>
 
    <main> 
      <div class="jumbotron">
        <img src="../assets/img/jumbotron.jpg" alt="">
      </div>
        
      <div class="series-container">
        <div class="wrapper container">

          <div 
          class="item"
          v-for="(serie,index) in series" :key="index"
          >
            <div class="img-container">
              <img :src="serie.thumb" alt="">
            </div>
            <div class="item-text">{{serie.series}}</div>
          </div>

        </div>
      </div>
      
    </main>
 
</template>


<script>
export default {
   name:'Main',
   props:['series'],
  
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
      .item{
        flex-basis: calc(100%/6);
        padding:10px;
        .img-container{
          height: 150px;
          width: 150px;
          overflow: hidden;
          img{
            width:150px;
          }
        }
        .item-text{
          color:white;
          font-size:13px;
          padding-top:20px ;
          max-width: 120px;
        }
      }
    }
  }

}
</style>

          
  
  