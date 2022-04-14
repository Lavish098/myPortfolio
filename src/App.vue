<template>
<div id="app" class="bg-gray-700">
  <div>
    <PageLoader />
    <NavigationMoblie/>
  <Navigation />
  <Home />
  <About />
  <Project />
  <Contact/>
</div>
  </div>
</template>

<script>
import Navigation from './components/navigation'
import NavigationMoblie from './components/navigationMobile'
import Home from './components/home'
import About from './components/about'
import PageLoader from './components/pageLoader.vue'
import Project from './components/project'
import Contact from './components/contact'

export default {
  name: 'App',
  components: {
    Navigation,
    NavigationMoblie,
    Home,
    About,
    PageLoader,
    Project,
    Contact
  },
  data(){
    return{

    }
  }
}
</script>

<style>
.project-card{
  display: grid;
  gap: 32px;
  grid-template-columns: 2fr;
}
.container {
  max-width: 1440px;
  margin: 0 auto;
}
</style>
