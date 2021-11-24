<template>
  <footer class="">
    <div class="top-footer container">
      <div class="footer-list-container">
        <ul v-for="(item,index) in footerList" :key="index">
          <li>{{item.footerListTitle}}</li>
          <li v-for="(subitem) in footerList[index].footerListitems" :key="subitem">{{subitem}}</li>
        </ul>
      </div>
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
footer{
   background-image: url("../assets/img/footer-bg.jpg");
   
}
.footer-list-container{
  display: flex;
  flex-wrap: wrap;
  width: 40%;
  padding:40px 0px1;
}
ul{
  width:100px;
}
li:first-child{
  color:white;
}
  li{
    list-style: none;
    color:grey;
  }

</style>

