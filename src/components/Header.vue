<template>
  <header>
      <!-- Top nav section -->
        <section id="top-nav" class="pt-1">
            <div class="container">
                <div class="row">
                    <div class="col-1 language d-flex align-items-center">
                        <div class="">English</div>
                        <i class="fas fa-angle-down px-2"></i>
                    </div>
                    <div class="col-11">
                        <!-- Link section -->
                        <ul class="d-flex justify-content-end m-0 ">
                            <li class="  text-center" v-for="(link,index) in topHeader" :key='index'>
                                <a class="px-2" href="#">
                                    {{link.type}} <span v-if="link.new===true" class="new">new</span>
                                </a>
                            </li>
                        <!-- Social Section -->
                            <ul class="d-flex justify-content-end ps-3">
                                <li v-for="(icon,index) in Social" :key="index">
                                    <a class="ps-2" href="#"><i class="social-icon" :class="socialGenerator(icon)"></i></a>
                                </li>
                            </ul>
                          
                        </ul>
                    </div>
                </div>
            </div>
        </section>
      <!-- Top nav section -->

      <!-- Bottom nav secrion -->
        <section id="bottom-nav" class="pt-4">
            <div class="container">
                <div class="row">
                    <div class="col-12 d-flex  align-items-center ">
                        <img class="main-logo" src="../assets/img/MasterStudy_logo.svg" alt="MasterStudy main logo">
                        <div class="ms-4 d-flex align-items-center flex-grow-1">
                            <i class="fas fa-bars"></i>
                            <span class="ms-1">CATEGORY</span>
                            <input type="text" class="ms-2 form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-lg" placeholder="Search courses">
                            <button class="btn  rounded-0"><i class="fas fa-search text-white fs-6"></i></button>
                        </div>   
                        <div class="ms-4 d-flex align-items-center ">
                            <i class="my_blue fas fa-bullhorn"></i>
                            <span class="ms-1">Become an instructor</span>
                            <i class="my_blue ms-4 fas fa-briefcase"></i>
                            <span class="ms-1">For Enterprise</span>
                        </div>
                        <div class="my_blue d-flex align-items-center ">
                            <i class="ms-4 far fa-user"></i>
                            <span class="ms-1">Log in</span>
                            <button class=" mx-4 btn rounded-pill text-white px-4 py-2">SIGN UP</button>
                            <i class="fs-5 far fa-bookmark"></i>
                        </div>
                    </div>
                </div>
            </div>
        </section>

      <!--/ Bottom nav secrion -->
    
  </header>
</template>

<script>
import topHeader from '../data/top-header.js'
import Social from '../data/social.js'
export default {
    name : 'Header',
    data: function(){
        return{
            topHeader,
            Social,
        }
    },
    methods:{
        socialGenerator: function(icon){
          return  icon.logo;
        }
    }
}
</script>

<style scoped lang='scss'>
@import '../style/varibles.scss';

    header{
        #top-nav{
            border-bottom: .7px solid #a3b4c3;
            font-size: 0.7rem;
            color: #97a9ba;
            line-height: 40px;
            
            .fas.fa-angle-down{
                cursor: pointer;
                 &:hover{
                        color: #7f8e9c;
                    }
            }
            ul{
                li{
                    position:relative;
                    .new{
                        position: absolute;
                        top: 0;
                        right: 0;
                        background-color: red;
                        color: white;
                        text-transform: uppercase;
                        line-height: 12px;
                        padding: 0 4px;
                        font-size: 0.5rem;
                    }
                }
                list-style-type: none;
                a{
                    text-decoration: none;
                    color: #97a9ba;
                    cursor: pointer;
                    &:hover{
                        color: #7f8e9c;
                    }
                }
                .social-icon{
                    color: #696b7a
                }
            }
        } 
        .my_blue{
            color: $primaryBlue;
        }  
        #bottom-nav{
            color: #7f8e9c;
           font-size: .8rem;
          
           .fas.fa-bars{
               font-size: .6rem;
           }
           input{
               background-color: #f0f2f5;
               
           }
           button{
               background-color: $primaryBlue;
               border-color: $primaryBlue;
           }
           button.rounded-pill{
               font-size: .8rem;
           }
        }
    }
</style>