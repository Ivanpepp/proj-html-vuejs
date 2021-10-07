<template>
    <div>


    <section id="proud-section" class="pt-4">
        <div class="container">
            <div class="row justify-content-center pt-5">
                <div class="col-5 text-center">
                    <h2>We are Proud</h2>
                    <p class="pt-2">
                        Certificate courses are instructed by highly educated and qualified instructors who hold doctoral and master's level degrees
                    </p>
                </div>
                
            </div>
            <div class="row  justify-content-center pt-5">
                <div v-for="(element,index) in proudResult" :key="index" class=" results col-2 text-center pt-5">
                    <h1>{{element.value}}</h1>
                    <p>{{element.name.toUpperCase()}}</p>
                </div>
            </div>
        </div> 
        
    </section>
    <section id="subscribe-section">
        <div class="container">
            <div class="row my_width text-white py-5">
                <div class="col-6">
                    <h4 class="fw-bold">Subscribe our newsletter</h4>
                    <p class="mb-0">There are many variations of passages of lorem impsum aviable, but the majority have suffered alteration in some form, by injected humor,or randomed words</p>
                </div>
                <div class="col-6">
                    <h4>YOUR EMAIL ADDRES</h4>
                    <div class="d-flex">
                        <input type="mail" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-lg" placeholder="Enter your E-mail">
                        <button class="btn  rounded-0">SUBSCRIBE</button>  
                    </div>
                    
                </div>
            </div>
        </div>
    </section>
    </div>
</template>

<script>
export default {
    name: 'Proud',
    data:function(){
        return{
           proudResult: [
               {
                   name: 'students',
                   value: 2000
               },
               {
                   name: 'courses',
                   value: 950
               },
               {
                   name: 'hours video',
                   value: 1600
               },
               {
                   name: 'countries reached',
                   value: 140
               },
               
           ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/varibles.scss';
    #proud-section{
        background-image: url('../assets/img/we_proud.png');
        height: 600px;
        margin: 0 auto;
        background-repeat: no-repeat;
        background-size: contain;
        background-position: bottom;
        background-color: #f0f4fa;
        font-family: $jumboFont;
        h2{
            font-size: rem;
        }
        p{
            color: rgb(170, 170, 170);
        }
        .results{
            
            border-right: 1px solid lightgray;
            }
            .col-2{
                h1{
                font-size: 4rem;
                
            }
            
            
        }
    }
    #subscribe-section{
        background-color: #4ed7a8;
    
        button{
            background-color: $primaryBlue;
            border-color: $primaryBlue;
            color: white;
        }
        h4{
            font-size: 1.3rem;
        }
        p{
                    font-size: 0.8rem;
                }
    }
</style>