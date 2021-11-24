<template>
  <div>
     <Header/>
     <Main/>
     <Content/>
     <Footer/>
  </div>
</template>

<script>
import Footer from './components/Footer.vue'
import Content from './components/Content.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'
export default {
  name: 'App',
  components: {
    Header:Header,
    Main:Main,
    Content:Content,
    Footer:Footer
  }
}
</script>

<style lang="scss">
@import"./assets/style/general.scss";

</style>
