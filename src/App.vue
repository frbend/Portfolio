<template>
  <div class="upperSection">
      <Landing></Landing>
      <Education></Education>
      <Work></Work>
      <Skills></Skills>
      <Footer data-aos="fade" data-aos-duration="1000"></Footer>
  </div>
</template>



<script>
import Landing from './components/Landing.vue'
import Education from './components/Education.vue'
import Work from './components/Work'
import Skills from './components/Skills'
import Footer from './components/Footer'
import AOS from 'aos'
import 'aos/dist/aos.css'


//TODO: subpage for japanese translations and repair exhibit
//TODO: rename sections in landing and make them center even if zoomed in/out

export default {
  name: 'App',
  mounted(){
    AOS.init()
  },
  components: {
    Landing,
    Education,
    Work,
    Skills,
    Footer,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oxygen:wght@300;400;700&display=swap');

#app {
  text-transform: uppercase;
  font-family: Oxygen, sans-serif;  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2A3250;
  margin-top: 60px;
}
  a:visited{
        color: #2A3250;
  }
</style>
