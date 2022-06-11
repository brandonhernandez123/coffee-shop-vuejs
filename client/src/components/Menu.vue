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
     <div v-for="pastry in pastries" :key="pastry.name" id="rowpastry" class="flip-card">
        
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
    <h4>Not sure what to get? Let us help</h4>
    <p>Hit the magic coffee button to get our recommendation</p>
    <button id="btn" v-on:click="getRandomCoffee()">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cup-straw" viewBox="0 0 16 16">
  <path d="M13.902.334a.5.5 0 0 1-.28.65l-2.254.902-.4 1.927c.376.095.715.215.972.367.228.135.56.396.56.82 0 .046-.004.09-.011.132l-.962 9.068a1.28 1.28 0 0 1-.524.93c-.488.34-1.494.87-3.01.87-1.516 0-2.522-.53-3.01-.87a1.28 1.28 0 0 1-.524-.93L3.51 5.132A.78.78 0 0 1 3.5 5c0-.424.332-.685.56-.82.262-.154.607-.276.99-.372C5.824 3.614 6.867 3.5 8 3.5c.712 0 1.389.045 1.985.127l.464-2.215a.5.5 0 0 1 .303-.356l2.5-1a.5.5 0 0 1 .65.278zM9.768 4.607A13.991 13.991 0 0 0 8 4.5c-1.076 0-2.033.11-2.707.278A3.284 3.284 0 0 0 4.645 5c.146.073.362.15.648.222C5.967 5.39 6.924 5.5 8 5.5c.571 0 1.109-.03 1.588-.085l.18-.808zm.292 1.756C9.445 6.45 8.742 6.5 8 6.5c-1.133 0-2.176-.114-2.95-.308a5.514 5.514 0 0 1-.435-.127l.838 8.03c.013.121.06.186.102.215.357.249 1.168.69 2.438.69 1.27 0 2.081-.441 2.438-.69.042-.029.09-.094.102-.215l.852-8.03a5.517 5.517 0 0 1-.435.127 8.88 8.88 0 0 1-.89.17zM4.467 4.884s.003.002.005.006l-.005-.006zm7.066 0-.005.006c.002-.004.005-.006.005-.006zM11.354 5a3.174 3.174 0 0 0-.604-.21l-.099.445.055-.013c.286-.072.502-.149.648-.222z"/>
</svg>
        Magic coffee button</button>
    <div v-for="coffee in randomcoffee" :key="coffee">
        <img v-bind:src='coffee' style="width:280px;height:225px;">
    </div>
</div>
</b-container>
</template>


<script>
import axios from 'axios'
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
            ],
            randomcoffee: ''
    }),
    mounted(){
        this.getRandomCoffee()
    },
    methods: {
        async getRandomCoffee(){
            const res = await axios.get('https://coffee.alexflipnote.dev/random.json')
            this.randomcoffee = res.data
            console.log(this.randomcoffee)
        }
    }
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
    width: 100%;
  
  margin: 0 auto;
  
}

#rowpastry{
    margin: 0 auto;
    width: 100%;
}

#btn{
    border-radius: 20px;
    background-color: rgb(117, 80, 80);
    color: white;
    margin-bottom: 10px;
}






</style>