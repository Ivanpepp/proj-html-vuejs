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
      <!-- popular section -->

      <section id="popular-section">
        <div  class="container">
            <div class="row justify-content-center pt-5">
              <h2 class="text-center pt-5 mb-3">Popular Courses</h2>
              <p class="text-center mb-4">Discover our most popular courses for self learnign</p>
              <Popular class="mb-5"  v-for="(card,index) in cardRecentCourses" :key='index' :card='card'/>
              <div class="page-slider mb-5">
                <i class=" fas fa-angle-left"></i>
                <i class=" fas fa-angle-right"></i>
              </div>
            </div>
        </div>
      </section>
      <!--/ popular section -->

      <!-- cta section -->
      <section id="cta">
       <div class="container py-3">
            <div class="row justify-content-between py-5">
              <div class="col">
                <div class="d-flex pe-3 box">
                  <img src="../assets/img/image_box_1-221x231.png" alt="Istructor image">
                  <div >
                    <h2 class="mb-3">Become an istructor</h2>
                    <p class="mb-3">Teach what you love. MasterStudy gives you the toolsto create a course.</p>
                    <button class="btn rounded-pill">start teaching</button>
                  </div>
                </div>
              </div>
              <div class="col">
                <div class="d-flex ps-3 box">
                  <img src="../assets/img/image_box_2-234x231.png" alt="Istructor image">
                  <div >
                    <h2 class="mb-3">Setup For Business</h2>
                    <p class="mb-3">Get unlmited access to 2.500 of Udemy's top courses for your team.</p>
                    <button class="btn rounded-pill">doing business</button>
                  </div>
                </div>
              </div>
            </div>
          </div>
      </section>      
      <!-- cta section -->

      <!-- Footer main Jumbo -->
      <section id="footer-main-jumbo">
       <div class="container py-3">
         <div class="row my_width py-5">
           <div class="col-7 p-5 bg-white">
             <h4>Come as you are</h4>
             <p class="mb-4">MasterStudy used is an excellent workshop whether you come as a counselor, advisor, administrator, or facutly member. I am going home empowered. I am looking forward toa ttending the On Course MasterStudy and the MasterStudy Nationale Conference next year and facilittating the use og this excellent retention/student succes course at mu college</p>
             <h5 class="fw-bold m-0">Tim Sab</h5>
             <span>General Developer, Stylemix Themes</span>
             <i class="fas fa-exclamation-triangle"></i>
           </div>
         </div>
       </div>
       
      </section>
      <!-- Footer main Jumbo -->
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
import Popular from './Popular.vue'
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
    Popular
    
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
            transition: .3s cubic-bezier(0.165, 0.84, 0.44, 1);
               &:hover{
                   background-color: blue;
                   border-color: blue;
                   transform: scale(1.3);
               }
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
    #popular-section{
      background-color: #f0f4fa;
      h2,p{
        font-family: $jumboFont;
      }
      p{
        color: rgb(182, 182, 182)
      }
      .page-slider{
        color: lightgray;
        text-align: center;
        font-size: 1.2rem;
        .fas{
          border: 1px solid lightgray;
          background-color: white;
          width: 40px;
          height: 40px;
          line-height: 40px;
        }
        .fas.fa-angle-left,
        .fas.fa-angle-right{
          transition: .3s cubic-bezier(0.165, 0.84, 0.44, 1);
          &:hover{
            background-color: #4ed7a8;
            border-color: #4ed7a8;
            color: white;
          }
        }
      }
    }
    #cta{
      .box{
        border: 1px solid lightgray;
        align-items: center;
        padding: 30px 0;
        img{
          padding: 30px;
          width: 300px;
        }
        button{
          background-color: $primaryBlue;
          border-color: $primaryBlue;
          text-transform: uppercase;
          color: white;
          transition: .1s cubic-bezier(0.165, 0.84, 0.44, 1);
               &:hover{
                   background-color: blue;
                   border-color: blue;
                   transform: scale(1.1);
                   
               }
        }
        p{
          color: rgb(180, 178, 178);
        }
      }
    }
    #footer-main-jumbo{
      background-image: url('../assets/img/brooke-cagle-224821-unsplash-1-1920x700.jpg');
      background-size: cover;
      .col-7{
        position: relative;
        .fa-exclamation-triangle{
        position: absolute;
        top: 50%;
        right: -30px;
        transform: translate(-50%);
        transform: rotate(90deg);
        color: white;
        font-size: 2rem;
        
      }
      p{
          color: rgb(193, 193, 193);
          font-family: $jumboFont;
        }
        h4{
          font-size: 1.8rem;
          font-family: $jumboFont;

        }
      }
      span{
        color: rgb(193, 193, 193);
      }
      
    }
</style>