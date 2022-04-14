<template>
    <div class=" text-black fixed md:-right-24 md:h-full  right-0 flex 
     w-20 md:w-44">
    <h1 class="hidden font-serif font-extrabold text-2xl p-4">{{ name }}</h1>
      <div class="hidden  md:block md:w-44 md:bg-green-400">
      <div class=" text-xl mt-8  leading-50px  
       "><a href="#home" class="flex"><i class="fas fa-home icon"></i>
       <h1 class="mt-4 px-5 py-4 text-xs font-medium">HOME</h1>
       </a></div>
          <div class=" text-xl mt-8   leading-50px
       " ><a href="#about"  class="flex"><i class="fab fa-audible icon"></i>
       <h1 class="mt-4 px-5 py-4 text-xs font-medium">ABOUT</h1></a></div>
          <div class=" text-xl mt-8  leading-50px
       " ><a href="#projects"  class="flex"><i class="fas fa-project-diagram icon"></i>
       <h1 class="mt-4 px-5 py-4 text-xs font-medium -ml-1">PROJECT</h1></a></div>
           <div class=" text-xl mt-8 leading-50px
       " ><a href="#contact"  class="flex"><i class="fas fa-id-badge icon"></i>
       <h1 class="mt-4 px-5 py-4 -ml-2 text-xs font-medium">CONTACT</h1></a></div>
       <div class="bottom-5  ml-3 fixed h-1/5">
        <a href="https://web.facebook.com/emmanuel.adeyemi.75286"><i class="fab fa-facebook-f p-4 cursor-pointer">
          </i></a><br>
        <a href="https://twitter.com/Adeyemimmanuel"><i class="fab fa-twitter p-4 cursor-pointer"></i></a><br>
        <a href="https://github.com/Lavish098"><i class="fab fa-github p-4 cursor-pointer"></i></a>
      </div>
      </div>
      
    </div>
</template>

<script>

export default {
  data(){
      return{
        name: 'LazyCode', 
        openNav: false,
      }
      
  },
  methods:{
      
  }
}
</script>
<style>
.btn-home .bar:nth-child(2) {
    opacity: 0;
  }
  .btn-home .bar:nth-child(1) {
    width: 2.25rem;
    height: 5px;
    transform: translateY(13px) rotate(45deg);
  }
  .btn-home .bar:nth-child(3) {
    width: 2.25rem;
    height: 5px;
    transform: translateY(-13px) rotate(-45deg);
  }
  .btn-home .bar{
    background: black;
    ;
  }
  .bar{
    transition: all ease-in-out 0.5s;
  }
    .btn-close{
    display: hidden;
  
  }
  
  .icon{
    padding: 10px;
    margin-top: 20px;
    margin-left: 20px;
    margin-right: 15px;
    transition: all ease-in 3s;
    transition-delay: 2s;
  }
  .icon:hover{
    display: none;
    /* margin-left: -80px; */
  }
@media screen and (max-width:500px) {
  .icon{
    padding: 10px;
    margin-top: 20px;
    margin-left: 10px;
    margin-right: 15px;
  }
}
</style>