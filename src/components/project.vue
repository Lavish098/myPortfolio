<template>
  <div class="projects container">
      <div class="text-center w-full ">
      <h1 class="pt-20 text-white text-3xl pb-8">{{ name }}</h1>
        </div>
        <div id="image" class="flex items-stretch flex-wrap card">
          <ProjectsCard />
        </div>
      
  </div>
</template>

<script>
import ProjectsCard from "./projectsCards.vue"
export default {
    components:{ ProjectsCard },
    data(){
        return{
            name: 'PROJECTS',
           
        }
    }
}
</script>

<style scoped>

#image {    
  animation: image 6s;
  position: relative;
}
@keyframes image{
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