<template>
  <main>
      <!-- Jumbo section -->
      <Jumbo />
      <!--/ Jumbo section -->

      <!-- Card section -->
      <Card  :cardBanner='cardBanner'/>
      <!-- Card section -->

      <!-- CoursesPreview section -->
      <CoursesPreview />
      <!--/ CoursesPreview section -->

       <!-- MidJumbo section -->
      <MidJumbo />
      <!--/ MidJumbo section -->
  </main>
</template>

<script>
import Jumbo from './Jumbo.vue'
import Card from './Card.vue'
import CoursesPreview from './CoursesPreview.vue'
import MidJumbo from './MidJumbo.vue'
import cardBanner from '../data/card'
export default {
  name: 'Main',
  data:function(){
    return{
      cardBanner,
    }
  },
  components:{
    Jumbo,
    Card,
    CoursesPreview,
    MidJumbo
  }
}
</script>

<style scoped lang='scss'>

</style>