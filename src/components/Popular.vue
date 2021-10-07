<template>
  <div v-if="card.popular==true" class="col-2 p-2">
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
    name: 'Popular',
    props:{
        card:{
            type: Object,
        }
    }
}
</script>

<style lang='scss'>

</style>