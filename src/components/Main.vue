<template>
  <main>
      <!-- Jumbo section -->
      <Jumbo />
      <!--/ Jumbo section -->

      <!-- Card section -->
      <div  class="container pt-5 mb-5" >
          <div class="row justify-content-between my_width">
            <Card  v-for="(card,index) in cardBanner" :key="index" :title='card.title' :paragraph='card.paragraph' :card='card'/>
          </div>
      </div>
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