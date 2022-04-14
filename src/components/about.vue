<template>
    <div id="about" class="w-full bg-white flex justify-center
    item-center pb-40">
        <div class="shadow-4x1 h-full md:w-4/5 md:mr-8 md:-ml-4 mt-12 
        lg:w-3/5 py-12 rounded-40px w-11/12 sm:ml-8">
          <h2 class="sm:mx-24 mx-8 w-10/12 sm:w-9/12 font-bold pb-8 text-4xl">About me</h2>
          <p class="md:ml-10 ml-4 w-11/12 lg:text-xl text-lg leading-40px
          md:text-xl md:leading-50px">I am a Front End Developer based in nigeria. I love to code and creating lovely
            and beautiful designs. My major programming language is HTML & CSS and my javascript 
            frame work is VUE. And i use FIREBASE for my Back-End.
          </p>
          <div class="flex justify-center items-center mt-8">
          <img :src="image1" alt="" class="image" id="image1">
          <img :src="image2" alt="" class="image" id="image2">
          <img :src="image3" alt="" class="image" id="image3">
          <img :src="image4" alt="" class="image" id="image4">
          </div>
        </div>
    </div>
</template>

<script>
export default {
  data(){
    return{
        image1: require('../assets/image/html5.png'),
        image2: require('../assets/image/css3.png'),
        image3: require('../assets/image/vue.png'),
        image4: require('../assets/image/firebase.png')
    
    }
  }
}
</script>
<style scoped>
.image{ 
  width: 90px;
  height: 90px;
  
}
@media screen and (max-width: 499px) {
  .image{ 
  width: 80px;
  height: 80px;
  
}
}
#image1 {    
  animation: image1 6s;
  position: relative;
}
@keyframes image1{
    0%{
      opacity: 0;
      z-index: 9999;
      left: -200px;
      top:0px
    }
    
    100%{
      opacity: 1;
      left: 10px;
      top:0px;
    }
}
#image2 {    
  animation: image2 6s ;
  position: relative;
}
@keyframes image2{
    0%{
      opacity: 0;
      z-index: 9999;
      left: -200px;
      top:0px
    }
    
    100%{
      opacity: 1;
      left: 10px;
      top:0px;
    }
}
#image3 { 
  position: relative;
  animation: image3 6s;
}
@keyframes image3{
    0%{
      opacity: 0;
      z-index: 9999;
      left: -200px;
      top:0px
    }
    
    100%{
      opacity: 1;
      left: 10px;
      top:0px;
    }
}
#image4 { 
  position: relative;
  animation: image4 6s;
}
@keyframes image4{
    0%{
      opacity: 0;
      z-index: 9999;
      left: -200px;
      top:0px
    }
    
    100%{
      opacity: 1;
      left: 10px;
      top:0px;
    }
}
</style>