<template>
   <header class="container">
     <div>
       <img src="../assets/img/dc-logo.png" alt="">
     </div>
     <div class="menu-right">
        <ul>
          <li v-for="(item,index) in menuList" :key="index" >
            <a :class="{'active': item.bool}" href=""><strong>{{item.content}}</strong></a>
          </li>     
        </ul>
      </div> 
   </header>
</template>
           
          
         
     


<script>

export default {
  name:'Header',
  data(){
    return{
      menuList:[
       { 
        content:'CHARACTERS',
        bool:false
        },
       { 
        content:'COMICS',
        bool:false
        },
       { 
        content:'MOVIES',
        bool:true
        },
       { 
        content: 'TV',
        bool:false
        },
       { 
        content:'GAMES',
        bool:false
        },
       { 
        content:'COLLECTIBLES' ,
        bool:false
        },
       { 
        content:'VIDEO',
        bool:false
        },
       { 
        content:'FANS',
        bool:false
        },
       { 
        content:'NEWS',
        bool:false
        },
       { 
        content:'SHOPS',
        bool:false
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/style/mixin.scss';
@import '../assets/style/vars.scss';
header{
  @include center($justify,$align)
 
}
.menu-right{
  width:60%;
  font-size:12px;
}
ul{
  // display:flex;
  // justify-content: space-around;
  @include center($justify,$align)
}
  li{
    &:hover a{
      color:#0288f9;
      border-bottom: 5px solid #0288f9;
     }
   a{
     display: block;
     height: 130px;
     line-height:130px;
     color:black;  
     padding:6px; 
   }
 }  
   
  .active{
    @include active();
   }


</style>

 

      