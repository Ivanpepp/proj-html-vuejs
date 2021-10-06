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
                            <div class="ms-3  d-flex justify-content-end">
                                <li v-for="(icon,index) in Social" :key="index">
                                    <a class="ps-3" href="#"><i class="social-icon" :class="socialGenerator(icon)"></i></a>
                                </li>
                            </div>
                          
                        </ul>
                    </div>
                </div>
            </div>
        </section>
      <!-- Top nav section -->
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
    header{
        #top-nav{
            border-bottom: .7px solid #a3b4c3;
            font-size: 0.8rem;
            color: #97a9ba;
            line-height: 50px;
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
    }
</style>