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
        transition: .3s cubic-bezier(0.165, 0.84, 0.44, 1);
        &:hover{
            transform: scale(1.1);
            box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
            border-radius: 30px;
        }
        h4{
            font-size: 1.2rem;
        }
        p{
            font-size: .8rem;
            color: rgb(151, 149, 149);
        }
        .card-logo{
            color: $primaryBlue;
            font-size: 3rem;
        }
    }
        
</style>