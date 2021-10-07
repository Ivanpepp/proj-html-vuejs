<template>
  <div class="col-2 p-2">
    <div class="card-wrapper ">
        <div class="image-course">
            <img :src="card.img" :alt="card.course" >
            <span v-if="card.hot===true" class="hot">hot</span>
            <span v-if="card.special===true" class="special">special</span>
            <span v-if="card.new===true" class="new">new</span>
            <span v-if="card.featured===true" class="featured">featured</span>
        </div>
        <div class="p-3">           
            <div class="course mb-2">{{card.course}}<i class=" ps-1 fas fa-angle-right"></i></div>
            <div class="mb-2">{{card.description}}</div>
            <div class="mb-3 line"></div>
            <div class="d-flex justify-content-between align-items-center">
                <div v-if="card.voteRequired === true" class="star-container d-flex">
                    <img class="star" v-for="(star,index) in card.vote" :key='index' src="../assets/img/starfull.svg" alt="star image">
                </div>
                <div v-if='card.voteRequired==false' class="course">
                    <i class="far fa-clock pe-1"></i> {{card.duration}}
                </div>
                <div>
                    {{card.price}}
                </div>
            </div>
        </div>  
    </div>
  </div>
</template>

<script>
export default {
    name: 'RecentCourses',
    props:{
        card:{
            type: Object
        },
     
    },
   
}
</script>

<style lang="scss" scoped>
@import '../style/varibles.scss';
    .image-course{
        position: relative;
        overflow: hidden;
         .hot{
            position: absolute;
            top: 5px;
            right: 5px;
            background-color: red;
            color: white;
            text-transform: uppercase;
            line-height: 12px;
            padding: 2px 5px;
            font-size: 0.7rem;
                    }
        .special{
            position: absolute;
            top: 5px;
            right: 5px;
            background-color: orange;
            color: white;
            text-transform: uppercase;
            line-height: 12px;
            padding: 2px 5px;
            font-size: 0.7rem;
        }
        .new{
            position: absolute;
            top: 5px;
            right: 5px;
            background-color: rgb(15, 185, 15);
            color: white;
            text-transform: uppercase;
            line-height: 12px;
            padding: 2px 5px;
            font-size: 0.7rem;
        }
        .featured{
        position: absolute;
        top: 15px;
        left: -25px;
        transform: rotate(320deg);
        background-color: orange;
        color: white;
        text-transform: uppercase;
        line-height: 12px;
        padding: 5px 30px;
        font-size: 0.7rem;
        font-weight: bold;
    }
    }
    .card-wrapper{
        border: 1px solid lightgray;
        transition: .3s cubic-bezier(0.165, 0.84, 0.44, 1);
        &:hover{
          border: 1px solid orange;    
        }
            .line{
            width: 100%;
            height: 1px;
            background-color: lightgray;
            }
         h2{
            font-family: $jumboFont;
            }
            img{
            width: 100%;
            object-fit: cover;
            object-position: center;
         }
         .course{
             color: lightgray;
             font-size: .8rem;
         }
         .star-container{
             .star{
                 width: 10px;
                 height: 10px;
             }
         }
         
    }
   
</style>