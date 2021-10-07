<template>
  <div class="pt-5 mb-5">
      <div id="jumbo">
          <div class="container">
              
              <div class="row my_width">
                    <div class="col-6 d-flex align-items-center">
                        <div class="text-start">
                            <h1 class="mb-4">Limitless learning, more possibilities</h1>
                            <p class="mb-4">With over 1200 courses in 18 subject, you're guaranteed to find something tht's right for you.</p>
                            <button class="btn rounded-pill text-white py-3 px-4">read more</button>
                        </div>
                    </div>  
              </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:'MidJumbo'
}
</script>

<style lang="scss" scoped>
@import '../style/varibles.scss';
#jumbo{
   
    font-family: $jumboFont;
    background-image: url('../assets/img/Untitled-1-1-1-1-1.png');
    background-position:center;
    height: 600px;
    .col-6{
        height: 600px;
         h1{
                font-size: 2.8rem;
            }
          button{
                background-color: $primaryBlue;
               border-color: $primaryBlue;
               text-transform: uppercase;
               font-weight: bold;
            }
    }
}
</style>