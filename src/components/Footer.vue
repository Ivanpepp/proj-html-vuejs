<template>
  <footer class="py-5">
      <div class="container">
        <div class="row my_width">
          <div class="col-3">
            <ul class="p-0 ls-none">
              <li v-for="(element,index) in foot" :key="index">
                <h4>
                  {{element.about.name}}
                </h4>
                <p><a class="my_blue" href="#">Masterstudy</a> is Education WordPress theme featured by learning Managment System (LMS) for online edcuation Developed by <a class="my_blue" href="#">Systemix Themes</a></p>
                <div class="social-container">
                  <i class="fab fa-facebook"></i>
                  <i class="fab fa-twitter"></i>
                  <i class="fab fa-instagram"></i>

                </div>
              </li>
            </ul>
          </div>
          <div class="col-2">
            <ul class="p-0 ls-none">
              <li v-for="(element,index) in foot" :key="index">
                  <h4>
                    {{element.contact.name}}
                  </h4> 
                  <p>{{element.contact.position}}</p>
                  <p>Tel.: {{element.contact.tel}}<br> 
                     Fax.: {{element.contact.fax}}</p>
                  
                  <p>{{element.contact.mail}}</p>
              </li> 
            </ul>
          </div>
           <div class="col-4">
            <ul class="ps-5 ls-none">
              <li class="ps-3" v-for="(element,index) in foot" :key="index" :class="pageDominator(element)">
                  <h4>
                    {{element.page.name}}
                  </h4> 
                  <ul class="ps-3 d-flex flex-wrap ">
                    <li  class="col-6 pb-1" v-for="(element,index) in page" :key="index" >
                      <a class="" href="#">
                        {{element}}
                      </a>
                    </li>
                  </ul>
              </li> 
            </ul>
          </div>
          <div class="col-3 p-0">
            <ul class="p-0 blog ls-none">
              <li v-for="(element,index) in foot" :key="index">
                <h4>
                  {{element.blog.name}}
                </h4>
               <div class="d-flex mb-3">
                 <img :src="element.blog.firstPost.img" alt="prova">
                  <div class="">
                    <p class="m-0 ps-2">{{element.blog.firstPost.title}}</p>
                    <span class="ps-2">--{{element.blog.firstPost.date}}</span>
                  </div>
               </div>
               <div class="d-flex">
                 <img :src="element.blog.secondPost.img" alt="prova">
                  <div>
                    <p class="m-0 ps-2">{{element.blog.secondPost.title}}</p>
                    <span class="ps-2">--{{element.blog.secondPost.date}}</span>
                  </div>
               </div>
              </li>
            </ul>
          </div>
        </div>
        
      </div>
  </footer>
</template>

<script>
import foot from '../data/footer'

export default {
  /* DATA */
  name: 'Footer',
  data: function(){
    return{
      foot,
      page:[],
     
    }
  },
  methods:{
    pageDominator: function(element){
      this.page = element.page.pages
      
    }
  }




}
</script>

<style lang="scss" scoped>
@import '../style/varibles.scss';
    footer{
      background-color: white;
      .social-container{
        color: rgb(176, 176, 176);
        .fab{
          margin-right: 15px;
        }
      }
      .my_blue{
        color: $primaryBlue;
      }
      .ls-none{
        list-style: none;
      }
      h4{
        font-size: 1rem;
        font-weight: bold;
      }
      a{
        font-size: .7rem;
        text-decoration: none;
        color: black;
      }
      p{
        font-size: .7rem;
      }
      img{
        object-position: center;
        object-fit: contain;
        
      }
      .blog{
        list-style: none;
        p{
          font-weight: bold;
          color: rgb(176, 176, 176);
          font-size: .8rem;
          line-height: 15px;
        }
        span{
          color: lightgray;
          font-size: .7rem;
        }
      }
    }
</style>