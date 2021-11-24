<template>
   <div>
     <div>
       <img src="" alt="">
     </div>
     <div class="menu-right">
        <ul>
          <li v-for="(item,index) in menuList" :key="index">{{item}}</li>     
        </ul>
      </div> 
   </div>
</template>
     


<script>

export default {
  name:'Header',
  data(){
    return{
      menuList:[
       'CHARACTERS',
       'COMICS',
       'MOVIES',
       'TV',
       'GAMES',
       'COLLECTIBLES',
       'VIDEO',
       'FANS',
       'NEWS',
       'SHOPS',
      ]
    }
  }
}
</script>

<style lang="scss">

.menu-right{
  width:60%;
  font-size:10px;
}
ul{
  display:flex;
  justify-content: space-around;
  li{
    list-style: none;
    &:hover{
      color:#0288f9
    }
  }
}

</style>