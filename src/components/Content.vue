<template>
  <div class="background">
    <div class="container">
      <ul>
        <li v-for="(item,index) in contentList" :key="index">{{item.menuItem}} <img :src="item.url" alt=""></li>     
      </ul>
    </div>
  </div> 
</template>

<script>
export default {
   name:'Content',
    data(){
    return{
      contentList:[
        {
          url:require('../assets/img/buy-comics-digital-comics.png'),
          menuItem:'DIGITAL COMIX',
        },
        {
          url:require('../assets/img/buy-comics-merchandise.png'),
          menuItem:'DC MERCHANDISE',
        },
        {
          url:require('../assets/img/buy-comics-shop-locator.png'),
          menuItem:'SUBSCRIPTION',
        },
        {
          url:require('../assets/img/buy-comics-subscriptions.png'),
          menuItem:'COMIC SHOP LOCATOR',
        },
        {
          url:require('../assets/img/buy-dc-power-visa.svg'),
          menuItem:'DC POWER VISA',
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss" >
@import '../assets/style/mixin.scss';
@import '../assets/style/vars.scss';
.background{
  background-color:#0282f9;

} 
ul{
  font-size:13px;
  @include center();
  padding:50px 0px;
  color:white;
  li{
    @include center();
    gap:10px;
    img{
      width:30px;
    }
  }
}
</style>
    
  
