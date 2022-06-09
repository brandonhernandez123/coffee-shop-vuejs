<template>
<div id="app">
 <header>
<NavBar />
 </header>
 <div class="content">
   <FeaturedComponent />
   <AboutUs id="about" />
  <MenuVue id="menu" />
 </div>
 </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import FeaturedComponent from './components/Featured.vue'
import AboutUs from './components/AboutUs.vue'
import MenuVue from './components/Menu.vue'

export default {
  name: 'App',
  components: {
   NavBar,
   FeaturedComponent,
  AboutUs,
  MenuVue
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Lobster&display=swap');
#app {
  font-family: 'Lobster', cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #fbeec1;
  height: 100%;
}

.content {
  margin-left: 200px;
  padding: 1px 16px;
  
  background-color: #fbeec1;
}




</style>
