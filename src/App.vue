<template>
  <div>
     <Header/>
     <Main/>
     <Content/>
  </div>
</template>

<script>
import Content from './components/Content.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'
export default {
  name: 'App',
  components: {
    Header:Header,
    Main:Main,
    Content:Content
  }
}
</script>

<style lang="scss">


</style>
