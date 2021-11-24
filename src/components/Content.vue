<template>
  <div class="">
    <ul>
      <li v-for="(item,index) in contentList" :key="index"><img src="item.menuIcon" alt=""> {{item.menuItem}}</li>     
    </ul>
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
          menuIcon:'../assets/img/buy-comics-digital-comics.png'
        },
        {
          menuItem:'DC MERCHANDISE',
          menuIcon:'../assets/img/buy-comics-merchandise.png'
        },
        {
          menuItem:'SUBSCRIPTION',
          menuIcon:'../assets/img/buy-comics-shop-locator.png'
        },
        {
          menuItem:'COMIC SHOP LOCATOR',
          menuIcon:'../assets/img/buy-comics-subscription.png'
        },
        {
          menuItem:'DC POWER VISA',
          menuIcon:'../assets/img/buy-comics-power-visa.svg'
        }
      ]
    }
  }
}
</script>

<style leng="scss" scoped>
ul{
  display:flex;
  justify-content: space-between;
  align-items: center;
  background-color:aqua;
  padding:50px 0px
}
</style>