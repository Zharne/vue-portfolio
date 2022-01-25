<template>
   <Navbar/> 
   <Home/>
   <About/>
   <Projects/>
   <Contact/>
   <Testimonials/>
</template>

<script>

import Home from './components/Home.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Navbar from './components/Navbar.vue'
import Contact from './components/Contact.vue'
import Testimonials from './components/Testimonials.vue'



export default {
  name: 'App',
  components: {
  Home, About, Projects, Navbar,
    Contact, Testimonials
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
