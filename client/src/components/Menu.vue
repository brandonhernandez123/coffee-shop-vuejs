<template>
<b-container fluid class="row">
    <h1 id='menu'>Menu</h1>
    <br/>
    <br/>
    <h5>Drinks</h5>
    <div v-for="product in products" :key="product.name" id="row" class="flip-card">
        
  <div :key='product.name' class="flip-card-inner">
    <div class="flip-card-front">
      <img v-bind:src='product.image' v-bind:alt='product.name' style="width:280px;height:225px;" id="productcard">
      <h2>{{product.name}}</h2>
    </div>
    <div  class="flip-card-back">
     
      <p>Ingridients: {{product.recipe}}</p>
      <p>${{product.price}}.00</p>
    </div>
  </div>
</div>
<div>
    <h5>Pastries</h5>
     <div v-for="pastry in pastries" :key="pastry.name" id="row" class="flip-card">
        
  <div :key='pastry.name' class="flip-card-inner">
    <div class="flip-card-front">
      <img v-bind:src='pastry.image' v-bind:alt='pastry.name' style="width:280px;height:225px;" id="productcard">
      <h2>{{pastry.name}}</h2>
    </div>
    <div  class="flip-card-back">
     
      <p> {{pastry.recipe}}</p>
      <p>${{pastry.price}}.00</p>
    </div>
  </div>
</div>
</div>
</b-container>
</template>


<script>

export default {
    name: 'MenuVue',
    data: () => ({
        products: [
        {
            name: 'Caramel Machiato',
            image: 'https://cooktoria.com/wp-content/uploads/2016/02/Caramel-Macchiato-Starbucks.jpg',
            recipe: '14 oz reduced fat or whole milk  2 tbsp vanilla syrup 2 oz espresso caramel sauce to drizzle',
            price: 3
        },
        {
            name: 'Cappucino',
            image: 'https://dairyfarmersofcanada.ca/sites/default/files/styles/recipe_image/public/image_file_browser/conso_recipe/2021/Italian%20Cappuccino.jpg.jpeg?itok=luefJXti',
            recipe: '1 shot of espresso 1/3 cup (80 mL) milk Pinch cinnamon',
            price: 5
        },
        {
            name: 'Chocolate Chip Frappe',
            image: 'https://www.dessertfortwo.com/wp-content/uploads/2022/01/Chocolate-Chip-Frappuccino-5.jpg',
            recipe: '1 cup milk 2 tablespoons sugar 1 teaspoon vanilla extract 3 tablespoons chocolate syrup, divided use 1/4 cup mini chocolate chips',
            price: 4
        },
        {
            name: 'Black Coffee',
            image: 'https://www.sharmispassions.com/wp-content/uploads/2021/05/BlackCoffee4-500x375.jpg',
            recipe: '1 cup water 1/2 tsp instant coffee powder 1/2 tsp sugar (optional)',
            price: 1
        }
        
        
        
        
        ],
        pastries:[
            {
                name: 'White Chocolate Walnut Muffins',
                image: 'https://imagesvc.meredithcorp.io/v3/mm/image?url=https%3A%2F%2Fstatic.onecms.io%2Fwp-content%2Fuploads%2Fsites%2F9%2F2016%2F09%2Fwhite-chocolate-walnut-muffins-xl-recipe0717.jpg',
                recipe: 'When white chocolate is baked into a muffin like this one little bits of it get toasty, caramelized and irresistible.',
                price: 5
            },
            {
                name: 'Fluffy, Buttery Cinnamon Rolls',
                image: 'https://imagesvc.meredithcorp.io/v3/mm/image?url=https%3A%2F%2Fstatic.onecms.io%2Fwp-content%2Fuploads%2Fsites%2F9%2F2016%2F10%2FHD-fw200602_cinnamonrolls.jpg',
                recipe: 'These Fluffy Buttery Cinnamon rolls will have you craving for days on end after you have had your first taste',
                price: 3
            },
            {
                name: 'Classic Croissants',
                image: 'https://imagesvc.meredithcorp.io/v3/mm/image?url=https%3A%2F%2Fstatic.onecms.io%2Fwp-content%2Fuploads%2Fsites%2F9%2F2020%2F08%2F21%2Fclassic-croissants-FT-RECIPE0920.jpg',
                recipe: 'Our Croissants are the best, come in and try yourself and you will be left in awe',
                price: 2
            },
            {
                name: 'Green Chile Spiced Apple Fritters',
                image: 'https://imagesvc.meredithcorp.io/v3/mm/image?url=https%3A%2F%2Fstatic.onecms.io%2Fwp-content%2Fuploads%2Fsites%2F9%2F2019%2F10%2F30%2Ffwcooks_spicedapplefritters_ft_recipe2019_235-2000.jpg',
                recipe: 'coated with a mixture of green chile powder and sugar.',
                price: 10
            }
            ]
    })
}
</script>

<style>
    .flip-card {
  background-color: transparent;
  width: 200px;
  height: 300px;
  border: 1px solid #f1f1f1;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

#menu{
    text-decoration-line: underline;
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the front side (fallback if image is missing) */
.flip-card-front {
  background-color: transparent;
  color: black;
}

/* Style the back side */
.flip-card-back {
  background-color: beige;
  color: black;
  transform: rotateY(180deg);
}

#row{
 display: grid;
  row-gap: 80px;
  grid-template-columns: auto ;
  
  margin: 0 auto;
  
}






</style>