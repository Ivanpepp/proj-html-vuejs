<template>
  <div id="app">
    <Header @search='searchNeedledCourses' />
    <Main :needle='needle' />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  data: function(){
    return{
      needle:'',
      filterCourse:[],
    }
  },
  components: {
    Header,
    Main,
    Footer
  },
  methods:{
    searchNeedledCourses: function(needle){
      this.needle = needle;
    },
  
  }
}
</script>

<style lang="scss">
@import './style/general.scss';
  #app{
    max-width: 1460px;
    margin: 0 auto;
  }  
    

</style>
