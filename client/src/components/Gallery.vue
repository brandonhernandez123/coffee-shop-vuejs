<template>
    <div class="row">
        <h2>Gallery</h2>
  <div class="column">
    <img :src="'https://st.depositphotos.com/1624098/1935/i/600/depositphotos_19354785-stock-photo-coffee.jpg'" >
    <img :src="'https://media.istockphoto.com/photos/come-join-us-for-a-coffee-picture-id1150956580?k=20&m=1150956580&s=612x612&w=0&h=A6xv5WT5YJtj-9eGHL17MZ0DFDIXjAZQbzVBGjYB7R0='" >
    <img :src="'https://images.unsplash.com/photo-1559925393-8be0ec4767c8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8c3RyZWV0JTIwY2FmZXxlbnwwfHwwfHw%3D&w=1000&q=80'">
    
  </div>
  <div class="column">
    <img :src="'https://images.lifestyleasia.com/wp-content/uploads/sites/7/2022/02/24115640/Untitled-design-2022-02-18T123717.280.jpg'">
    <img :src="'https://assets.architecturaldigest.in/photos/606c36d0e530975c04f31855/master/pass/Surat%20Restro%20Qualia%20cafe%20interiors.jpg'">
    <img :src="'https://cdn.shopify.com/s/files/1/0514/4284/3810/products/Cafe_Gratitude-Meal_Plans-JStrutz-042921-0711_600x.jpg?v=1628641739'">
   
  </div>

   <div class="column">
    <img :src="'https://www.incimages.com/uploaded_files/image/1920x1080/getty_938993594_391384.jpg'" >
    <img :src="'https://content-prod-live.cert.starbucks.com/binary/v2/asset/137-78062.jpg'" >
    <img :src="'https://cdn.vox-cdn.com/thumbor/qXyyt4MLLFw8O6wpkYry_0g8H0w=/0x0:1200x800/1200x800/filters:focal(504x304:696x496)/cdn.vox-cdn.com/uploads/chorus_image/image/61385583/BlueSparrowCoffee.0.jpg'">
   
  </div>
   <div class="column">
    <img :src="'https://bunniwolf.com/wp-content/uploads/2019/02/hf-ragoussis-bakery-bistro-eatery-delivery-food-online-coffee-pastry-sweets-breakfast-lunch-paros-naoussa-greece-photo11.jpg'">
    <img :src="'https://i.pinimg.com/originals/1f/96/ae/1f96aea25041319b5654ca2f3d60573c.jpg'">
   
  </div>
  </div>
</template>

<script>
export default {
    name: 'GalleryVue'
}
</script>

<style>
.row {
  display: flex;
  flex-wrap: wrap;
  padding: 0 4px;
}

/* Create four equal columns that sits next to each other */
.column {
  flex: 25%;
  max-width: 25%;
  padding: 0 4px;
}

.column img {
  margin-top: 8px;
  vertical-align: middle;
  width: 100%;
}

/* Responsive layout - makes a two column-layout instead of four columns */
@media screen and (max-width: 800px) {
  .column {
    flex: 50%;
    max-width: 50%;
  }
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column {
    flex: 100%;
    max-width: 100%;
  }
}
</style>