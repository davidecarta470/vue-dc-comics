<template>
  <footer>
    <div class="top-footer">
      <ul v-for="(item,index) in footerList" :key="index">
        <li>{{item.footerListTitle}}</li>
        <li v-for="(subitem,index) in footerListitems" :key="index">{{subitem}}</li>
      </ul>
    </div>
    <div class="bottom-footer">

    </div>
  </footer>
</template>

<script>
export default {
   name:'Footer',
   data(){
    return{
      footerList:[
        {
          footerListTitle:'DC COMIX',
          footerListitems:[
             'Characters',
             'Comics',
             'Movies',
             'TV',
             'Games',
             'Videos',
             'News'
          ]
        },
        {
          footerListTitle:'DC',
          footerListitems:[
            'Term Of Use',
            'Privacy policy(New)',
            'Ad Choices',
            'Advertising',
            'Jobs',
            'Subscription',
            'Talent Workshop',
            'CPSC Certificates',
            'Rating',
            'Shop Help'
          ]
        },
        {
          footerListTitle:'SITES',
          footerListitems:[
            'Term Of Use',
            'Privacy policy(New)',
            'Ad Choices',
            'Advertising',
     
          ]
        },
        {
          footerListTitle:'SHOP',
          footerListitems:[
            'Term Of Use',
            'Privacy policy(New)',
          
    
          ]
        },

      ]
    }
  }
}
</script>

<style scoped leng="scss">
.top-footer{
   background-image: url("../assets/img/footer-bg.jpg");
   height:500px;
}
ul{
  color:white;
  list-style: none;
}

</style>

