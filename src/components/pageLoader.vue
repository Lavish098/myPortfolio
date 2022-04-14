<template>
    <div class="loader text-white" v-if="!isloaded">
        <div class="screenload">
        <h1 class="font-serif text-7xl flex justify-center
        text-green-400">{{ typeValue }}</h1>
    </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            isloaded: false,  
          typeValue: '',
          typeStatus: false,
          typeArray:["AIRE STUDIO"],
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
    },
    mounted(){
        document.onreadystatechange = () =>{
            if(document.readyState == "complete"){
                this.isloaded= true;
            }
        }
    }
}
</script>
<style>
.loader{
    display: flex;
    position: fixed;
    width: 100vw;
    height: 100vh;
    background: black;
    /* z-index: 999; */
}
.screenload{
    display: flex;
    position: fixed;
    justify-content: center;
    align-items: center;
    top: 50%;
    left: 20%;
    justify-content: center;
    align-items: center;
    
}
.circle1 {    
    position: absolute;
    
  animation: circle1 5s infinite;
}
@keyframes circle1{
    from{
        transform: rotate(0);
    }
    to{
        transform: rotate(360deg);
    }
}
.circle2 {
    position: absolute;
  animation: circle2 5s infinite;
}
@keyframes circle2{
    from{
        transform: rotate(0);
    }
    to{
        transform: rotate(360deg);
    }
}
.circle3 {
    position: absolute;
    
  animation: circle3 5s infinite;
}
@keyframes circle3{
    from{
        transform: rotate(0);
    }
    to{
        transform: rotate(360deg);
    }
}

</style>