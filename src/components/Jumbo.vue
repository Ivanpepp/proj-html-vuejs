<template>

  <section id="jumbo-section" class="mt-5" >
      <div class="container ">
          <div class="row my_width pt-5">
              <div class="col-6 d-flex flex-column justify-content-center">
                  <h1 class="mb-4">Start Investing in You</h1>
                  <p class="mb-4">With over 1200 courses in 18 subject, you're guaranteed to find something tht's right for you.</p>
                  <button class="btn rounded-pill text-white">join for free</button>
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
    #jumbo-section{
        .col-6{
            height: 500px;
            button{
                background-color: #1a5eca;
               border-color: #1a5eca;
            }
            .book-1{
            
            position: relative;
            bottom: 365px;
            left: 370px;
        }
        .book-2{
            position: relative;
            bottom: 390px;
            left: 220px;
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