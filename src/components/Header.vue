<template>
   <header class="container">
     <div>
       <img 
        @click="active=-1"
        src="../assets/img/dc-logo.png" alt=""
       >
     </div>
     <div class="menu-right">
        <ul>
          <li v-for="(item,index) in menuList" :key="index" >
            <a 
            @click="active = item" 
            :class="{'active': active === item}"
            href="#"><strong>{{item.content}}</strong></a>
          </li>     
        </ul>
      </div> 
   </header>
</template>
       
           

<script>
import menuList from '../assets/data/menuList'
export default {
  name:'Header',
  data(){
    return{
      active:-1,
      menuList 
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/style/mixin.scss';
@import '../assets/style/vars.scss';
header{
  @include center()
 
}
.menu-right{
  width:60%;
  font-size:12px;
}
ul{
  @include center($justify)
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

 
          
         
     


      