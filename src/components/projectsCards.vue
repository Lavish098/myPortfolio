<template>
   <div class="project-card" v-for="project in projects" :key="project">
            <a :href="project.url">
            
            <img :src="require(`../assets/image/${project.image}.jpeg`)" alt="">
            <h2>{{ project.title}}</h2>
           
            </a>
            </div>
</template>

<script>
export default {
    name: "projectsCard",
    props:["post"],
data(){
    return{
         projects:[
                   {title:'SavBlog', url:'https://savblog.site', image:'Home _ SavBlog'},
                   
            ]
    }
}
}
</script>

<style scoped>
.project-card{
    position: relative;
    cursor: pointer;
    margin-left: 30px;
    margin-right: 30px;
    margin-bottom: 20px;
    width: 100%;
    padding-bottom: 10px;
    border-radius: 8px;
    background-color: #fff;
    min-height: 20px;
    transition: .5s ease all;
}
@media screen and (min-width: 600px){
    .project-card{
        width: 42%;
        margin-left: 20px;
        margin-right: 0px;
    }
}
@media screen and (min-width: 700px){
    .project-card{
        width: 40%;
        margin-left: 30px;
    }
}
@media screen and (min-width: 900px){
    .project-card{
        width: 25%;
        margin-left: 35px;
    }
}
@media screen and (min-width: 1200px){
    .project-card{
        width: 20%;
        margin-left: 25px;
    }
}

.project-card:hover{
    transform: rotateZ(-2deg) scale(1.01);
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.86);
}
.project-card img{
    border-radius: 8px 8px 0 0;
    z-index: 1;
    width: 100%;
    min-height: 100px;
    object-fit: cover;
}
/* .project-card-content{
    display: flex;
    position: relative;
    width: 90%;
} */
a{
    font-size: 30px;
    font-weight: bold;
    font-family: 'Courier New', Courier, monospace;
    color: rgb(57, 63, 82);
}
.project-card h2{
    margin-left: 10px;
}
</style>