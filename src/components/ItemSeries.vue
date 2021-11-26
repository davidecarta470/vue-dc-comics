<template>
    <div class="item" >
      <div class="img-container">
        <img :src="serieImage" alt="">
      </div>
      <div class="item-text">{{serieName}}</div>
    </div>
</template>

<script>
export default {
  name: 'ItemSeries',
  props:{
    serieImage: String,
    serieName: String
  }
}
</script>

<style scoped lang="scss">
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
</style>
     
        

          
          
         
