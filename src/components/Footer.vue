<template>
  <footer class="">
    <div class="top-footer container">

      <div class="second-background">
        <div class="footer-list-container ">

          <ul v-for="(item,index) in footerList" :key="index">
            <li>{{item.footerListTitle}}</li>
            <li v-for="(item) in footerList[index].footerListitems" :key="item">{{item}}</li>
          </ul>
        </div>
      </div>
      
    </div>
    <div class="bottom-footer">
      <div class="container">
        <div>
         <button>SIGN-UP NOW!</button>
        </div>
        <div class="bottom-right-container">
          <span>FOLLOW US!</span>
          <ul><li v-for="item in socialLinks" :key="item"><img :src="item" alt=""></li></ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import footerList from '../assets/data/footerList'

export default {
   name:'Footer',

   data(){
    return{
      footerList,
      socialLinks:[
          require('../assets/img/footer-facebook.png'),
          require('../assets/img/footer-periscope.png'),
          require('../assets/img/footer-pinterest.png'),
          require('../assets/img/footer-twitter.png'),
          require('../assets/img/footer-youtube.png'),
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import"../assets/style/mixin.scss";


footer{
  background-image: url("../assets/img/footer-bg.jpg");
  background-size:cover;
   .second-background{
        background-image: url("../assets/img/dc-logo-bg.png"); 
        background-repeat:no-repeat;
        background-position:right;
   }
   .footer-list-container{
        display: flex;
        flex-wrap: wrap;
        width: 400px;
        padding:40px 0px;
        flex-basis: calc(100%/3);
        gap: 0px 40px;
        
          li{
            text-align: justify;
            list-style: none;
            color:lightgrey;
            font-size:10px;
            padding-top:10px;
            &:hover{
              color:white;
              transform: scale(1.2);
            }
          }
          li:first-child{
            font-weight: bold;
            color:white;
            padding-bottom: 15px;
            font-size:18px;
            &:hover{
              color :none;
              transform: none;
            }
          }
          
  }
@import"../assets/style/vars.scss";
  .bottom-footer{
    background-color:#303030;
    height:100px;
    display: flex;
    .container{
      @include center();
      button{
        border:2px solid #0282f9;
        color :white;
        padding: 10px;
        background-color:transparent;
      }
      .bottom-right-container{
        @include center($align);
        ul{
          display: flex;
          li{
            padding-left: 20px;
          }
        }
        span{
          align-self: center;
          color: #0282f9;
        }
      }
    }
  }
}
      
</style>





