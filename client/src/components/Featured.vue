<template>
    <div class="featured">
        <h1 id="featuredtitle">Welcome to Coffee Shop.</h1>
        <br/>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-width="1024"
    img-height="180"
  >
    <b-carousel-slide
      
      img-src="https://i.imgur.com/SWEK4JT.png"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="Try one of our delicious frappe's"
      img-src="https://i.imgur.com/7kqOSEQ.png"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="our signature Croissants will brighten your day in 2.5 seconds"
      img-src="https://i.imgur.com/7O99A89.png"
    ></b-carousel-slide>
  </b-carousel>
</div>
</template>


<script>
export default {
    name: 'FeaturedComponent'
}
</script>


<style>
.featured{
    text-align: center;
}

#featuredtitle{
    text-decoration-line: underline;
    font-size: 80px;
}
</style>