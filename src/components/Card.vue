<template>
  <div  class="container pt-5 mb-5" >
      <div class="row justify-content-between my_width">
            <div v-for="(card,index) in cardBanner" :key="index" class="col">
                <i class="card-logo mb-4" :class="cardLogoGenerator(card)"></i>
                <h4 class="mb-4">{{card.title}}</h4>
                <p>{{card.paragraph}}</p>
            </div>
      </div>  
  </div>
</template>

<script>
export default {
    name: 'Card',
    props:{
        cardBanner:{
            type: Array,
        }
    },
    methods:{
        cardLogoGenerator: function(card){
            return card.logo;
        }
    }
}
</script>

<style scoped lang='scss'>
@import '../style/varibles.scss';

    h4{
        font-size: 1.1rem;
    }
    p{
        font-size: .7rem;
    }
    .card-logo{
        color: $primaryBlue;
        font-size: 3.5rem;
    }
</style>