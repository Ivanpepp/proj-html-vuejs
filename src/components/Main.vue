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

      <div id="recent-courses-section" class="container pt-5 mb-5 ">
        <div class="row justify-content-center">
          <h2 class="text-center fs-1 mb-5">Recent courses</h2>
          <nav class="mb-5">
            <ul class="d-flex justify-content-center">
              <li class="mx-1 "  v-for="(course,index) in navRecentCourses" :key='index'>
               <a @click='isActive(index)' :class="{'active' : index == indexCounter}"  href="#recent-courses-section"> {{course.name}} </a>
              </li>
            </ul>
          </nav>
          <RecentCourses class="mb-4" v-for="(card,index) in cardRecentCourses" :key="index" :card='card' />
          <div class="text-center pt-5 mb-3">
            <button id="my_button" class="btn text-white  rounded-pill py-2 px-4 mb-5">show all</button>
          </div>
          <div class="stiker-container shadow">
            <ul class="p-0 m-0 d-flex flex-column align-items-center justify-content-around ">
              <li><a href="#"><i class="fas fa-desktop"></i></a></li>
              <li><a href="#"><i class="far fa-circle"></i></a></li>
              <li><a href="#"><i class="fas fa-wrench"></i></a></li>
              <li><a href="#"><i class="fas fa-shopping-cart"></i></a></li>
              <li><a href="#"><i class="fas fa-mobile-alt"></i></a></li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Recent Courses section -->
      
      <!-- Proud section -->
      <Proud />
      <!-- Proud section -->

  </main>
</template>

<script>
/* COMPONENTS */
import Jumbo from './Jumbo.vue'
import Card from './Card.vue'
import CoursesPreview from './CoursesPreview.vue'
import MidJumbo from './MidJumbo.vue'
import RecentCourses from './RecentCourses.vue'
import Proud from './Proud.vue'
/* DATA */
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
    Proud,
    
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

    #recent-courses-section{
      position:relative;
      nav{
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
      }
      
      button{
          background-color: $primaryBlue;
            border-color: $primaryBlue;
            text-transform: uppercase;
            font-weight: bold;
        }
      .stiker-container{
        position: absolute;
        bottom: 0;
        right: -70px;
        padding: 0;
        width: 50px;
        height: 200px;
        background-color: white;
        ul{
          list-style-type: none;
          height: 100%;
          a{
            color: black;
          }
        }
        
      }
    }
     
</style>