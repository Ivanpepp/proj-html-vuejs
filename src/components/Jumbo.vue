<template>

  <section id="jumbo-section" class="mt-5" >
      <div class="container ">
          <div class="row my_width pt-5">
              <div class="col-6 d-flex  align-items-center">
                    <div class="text-start">
                        <h1 class="mb-4">Start Investing in You</h1>
                        <p class="mb-4">With over 1200 courses in 18 subject, you're guaranteed to find something tht's right for you.</p>
                        <button class="btn rounded-pill text-white py-2 px-3">join for free</button>
                    </div>
                    
              </div>
              <div class="col-6">
                  
                  <img class="base" src="../assets/img/base.png" alt="">
                  <img class="book-1" src="../assets/img/book1.png" alt="">
                  <img class="book-2" src="../assets/img/book2.png" alt="">
                  <img class="bubblespeech" src="../assets/img/bubblespeech.png" alt="">
                  <img class="magnifier" src="../assets/img/magnifier.png" alt="">
                  
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Jumbo',
}
</script>

<style scoped lang='scss'>
@import '../style/varibles.scss';

    #jumbo-section{
        font-family: $jumboFont;
        color: $jumboColor;
        .col-6{
            height: 500px;
            h1{
                font-size: 2.8rem;
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
                }
            }

            .book-1{
            
            position: relative;
            bottom: 365px;
            left: 370px;
                -webkit-animation:spin 3s linear  ;
                -moz-animation:spin 3s linear  ;
                animation:spin 3s linear  ;
                }
                @-moz-keyframes spin { 
                    100% { -moz-transform: rotate(360deg); } 
                }
                @-webkit-keyframes spin { 
                    100% { -webkit-transform: rotate(360deg); } 
                }
                @keyframes spin { 
                    100% { 
                        -webkit-transform: rotate(360deg); 
                        transform:rotate(360deg); 
                    } 
                
        }
        .book-2{
            position: relative;
            bottom: 390px;
            left: 220px;
                -webkit-animation:spin 3s linear  ;
                -moz-animation:spin 3s linear  ;
                animation:spin 3s linear  ;
                }
                @-moz-keyframes spin { 
                    100% { -moz-transform: rotate(-360deg); } 
                }
                @-webkit-keyframes spin { 
                    100% { -webkit-transform: rotate(-360deg); } 
                }
                @keyframes spin { 
                    100% { 
                        -webkit-transform: rotate(-360deg); 
                        transform:rotate(-360deg); 
                    } 
                
        }
        .bubblespeech{
            position: relative;
            bottom: 640px;
            left: 255px; 
        }
        .magnifier{
            position: relative;
            bottom: 395px;
            left: 150px; 
        }
        }
         
    }
       

</style>