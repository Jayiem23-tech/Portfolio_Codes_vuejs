<template>
  <div id="app"> 
   
      <Nav/> 
      <Home class="banner">
        <vue-particles color="#dedede"
                          :particleOpacity="0.7"
                          :particlesNumber="20"
                          shapeType="edge"
                          :particleSize="13"
                          linesColor="#dedede"
                          :linesWidth="0"
                          :lineLinked="false"
                          :lineOpacity="0.5"
                          :linesDistance="150"
                          :moveSpeed="1"
                          :hoverEffect="false" 
                          :clickEffect="false" 
                          class="design" />
          </Home >
          
    <Project/> 
    <Skills/>
    <About/>
    <Footer/>     
  </div>
</template>

<script>
import Nav from './components/nav.vue'
import Home from './components/home.vue'
import Project from './components/projects.vue'
import Skills from './components/skills.vue' 
import About from './components/about.vue'
import Footer from './components/footer.vue' 
export default {
  name: 'App',
  components: {
    Nav,
    Home,
    Project,
    Skills,
    About,
    Footer
  }
}
</script>

<style>
html{
   scroll-behavior: smooth;
}
body{ 
    margin:0px;
    padding:0px; 
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; 
}
 



 
 

</style>
