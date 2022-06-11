<template>
<div id="app">
 <header>
<NavBar />
 </header>
 <div class="content">
   <FeaturedComponent />
   <AboutUs id="about" />  
   <GalleryVue id="gallery" />
   <br/>
   <br/>
  <MenuVue id="menu" />
  <ContactForm id="contact" />
  <br>
  <footer>
   <FooterVue id="footer" />
 </footer>  
 </div>

 
 </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import FeaturedComponent from './components/Featured.vue'
import AboutUs from './components/AboutUs.vue'
import MenuVue from './components/Menu.vue'
import GalleryVue from './components/Gallery.vue'
import ContactForm from './components/Contact.vue'
import FooterVue from './components/Footer.vue'


export default {
  name: 'App',
  components: {
   NavBar,
   FeaturedComponent,
  AboutUs,
  MenuVue,
  GalleryVue,
  ContactForm,
  FooterVue
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
  background-color: #B18F6A;
  height: 100%;
}

.content {
  margin-left: 200px;
  padding: 1px 16px;
  
  background-color: #fbeec1;
}

#about{
  margin-top: 80px;
}

#gallery{
  margin-top: 200px;
  background-color: #7B3F00;
  color: white;
}

#contact{
  margin-top: 250px;
}

#footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  margin: 0 auto;
  background-color: #7B3F00;
  color: white;
  text-align: center;
}





</style>
