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
          menuItem:'DIGITAL COMIX',
          url:'../assets/img/buy-comics-digital-comics.png'
        },
        {
          menuItem:'DC MERCHANDISE',
          url:'../assets/img/buy-comics-merchandise.png'
        },
        {
          menuItem:'SUBSCRIPTION',
          url:'../assets/img/buy-comics-shop-locator.png'
        },
        {
          menuItem:'COMIC SHOP LOCATOR',
          url:'../assets/img/buy-comics-subscription.png'
        },
        {
          menuItem:'DC POWER VISA',
          url:'../assets/img/buy-dc-power-visa.svg'
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
  @include center($justify,$align);
  padding:50px 0px;
  color:white
}
</style>