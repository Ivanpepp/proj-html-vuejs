<template>
            <div  class="col">
                <i class="card-logo mb-4" :class="cardLogoGenerator(card)"></i>
                <h4 class="mb-4">{{title}}</h4>
                <p>{{paragraph}}</p>
            </div>
</template>

<script>
export default {
    name: 'Card',
    props:{
        title:{
            type: String,
        },
        paragraph:{
            type: String,
        },
        card:{
            type: Object
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

    .col{
        background-color: #f2f6fb;
        padding: 20px;
        &:nth-child(2){
            margin: 0px 20px;
        }
        h4{
            font-size: 1rem;
        }
        p{
            font-size: .6rem;
        }
        .card-logo{
            color: $primaryBlue;
            font-size: 3rem;
        }
    }
        
</style>