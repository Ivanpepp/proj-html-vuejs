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

      <!-- Recent Courses section -->

      <div id="recent-courses-section" class="container pt-5">
        <div class="row">
          <h2 class="text-center fs-1 mb-5">Recent courses</h2>
          <nav class="mb-5">
            <ul class="d-flex justify-content-center">
              <li class="mx-1 "  v-for="(course,index) in navRecentCourses" :key='index'>
               <a @click='isActive(index)' :class="{'active' : index == indexCounter}"  href="#recent-courses-section"> {{course.name}} </a>
              </li>
            </ul>
          </nav>
          <RecentCourses  />
        </div>
      </div>

      <!-- Recent Courses section -->
      

  </main>
</template>

<script>
import Jumbo from './Jumbo.vue'
import Card from './Card.vue'
import CoursesPreview from './CoursesPreview.vue'
import MidJumbo from './MidJumbo.vue'
import RecentCourses from './RecentCourses.vue'
import cardBanner from '../data/card'
import navRecentCourses from '../data/nav-recent-courses'
import cardRecentCourses from '../data/card-recent-courses'
export default {
  name: 'Main',
  data:function(){
    return{
      cardBanner,
      navRecentCourses,
      cardRecentCourses,
      indexCounter: 0,
    }
  },
  components:{
    Jumbo,
    Card,
    CoursesPreview,
    MidJumbo,
    RecentCourses,
    
  },
  methods:{
    isActive: function(index){
      this.indexCounter = index
    }
  }
}
</script>

<style scoped lang='scss'>
@import '../style/varibles.scss';
  ul{
    list-style-type: none;
    a{
      text-decoration: none;
      color: $primaryBlue;
      padding: 10px 20px;
      transition: .2s cubic-bezier(0.165, 0.84, 0.44, 1);
       &:hover{
        background-color: #f0f4fa;
        color: #bfc1c3;
        border-radius: 20px;

    }
    }
    .active{
      background-color: #f0f4fa;
      color: #bfc1c3;  
      border-radius: 20px;
    }
   
  }
</style>