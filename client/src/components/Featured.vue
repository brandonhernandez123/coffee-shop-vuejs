<template>
    <div class="featured">
        <h1 id="featuredtitle">Our Featured items!</h1>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-width="1024"
    img-height="480"
  >
    <b-carousel-slide
      
      img-src="https://i.imgur.com/SWEK4JT.png"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="Try one of our delicious frappe's"
      img-src="https://i.imgur.com/7kqOSEQ.png"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="Croissants?"
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
}
</style>