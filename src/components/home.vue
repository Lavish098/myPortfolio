<template>
 <div id="home" class="bg-gray-700 h-full px-0 py-60 flex flex-col justify-center items-center
 container max-w-full sm:py-52 md:py-56 lg:py-72 md:text-center text-white
 ">
     <h2 class="md:ml-6 md:mr-0 font-bold font-serif leading-50px
     text-5xl ml-12 sm:ml-0 sm:w-2/3 w-4/5 mt-8 h-40
     lg:ml-0 lg:w-1/2 md:text-7xl lg:text-7xl sm:text-6xl text-green-400">
          {{ typeValue }}<span class="span">&nbsp;</span>
        </h2>
        <p class="md:ml-4 md:mr-0 sm:ml-8 mt-4 sm:mt-1 sm:text-lg sm:pt-3 
        sm:mr-8 smm:ml-0
        md:text-lg lg:mt-1 lg:text-xl lg:ml-40 lg:mr-44 text-sm text-center">
          Front End Developer / Web Developer
        </p>

 </div>
 
 
</template>


<script>
export default {
    data(){
        return{
          
          typeValue: '',
          typeStatus: false,
          typeArray:["I'm Adeyemi Emmanuel"],
          typingSpeed:200,
          erasingSpeed:200,
          newTextDelay:200,
          typeArrayIndex:0,
          charIndex:0
        }
    },
    methods:{
      typeText(){
        if(this.charIndex < this.typeArray[this.typeArrayIndex].length){
          if(!this.typeStatus)
          this.typeStatus = true;

          this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
          this.charIndex += 1;
          setTimeout(this.typeText,  this.newTextDelay);
        }else{
          this.typeStatus = false;
          setTimeout(this.eraseText, this.newTextDelay)
        }
      },
      eraseText(){
        if(this.charIndex > 0){
          if(!this.typeStatus)
          this.typeStatus = true;

          this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
          this.charIndex -= 1;
          setTimeout(this.eraseText, this.erasingSpeed)
        }else{
          this.typeStatus = false;
          this.typeArrayIndex += 1;
          if(this.typeArrayIndex >= this.typeArray.length)
          this.typeArrayIndex = 0;
          setTimeout(this.typeText, this.typingSpeed + 100)
    }
      }
    },
    created(){
      setTimeout(this.typeText, this.newTextDelay + 200)
    }
}
</script>
<style>
.span{
  width: 2px;
  height: 10px;
  background: white;
}
</style>