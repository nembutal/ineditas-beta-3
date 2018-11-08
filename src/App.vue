<template>
  <div id="app">
    <router-view/>
    <Caja/>
    <Footer/>
  </div>
</template>

<script>
import Caja from './components/caja.vue'
import Footer from './components/footer.vue'
export default {
  name: 'App',
  components:{
    Caja,
    Footer
  }
}
</script>

<style>
*{
  padding:0px;
  margin:0px;
  box-sizing: border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
