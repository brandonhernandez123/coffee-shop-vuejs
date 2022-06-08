<template>
    <div class="row">
        <h2>Gallery</h2>
  <div class="column">
    <img src='https://st.depositphotos.com/1624098/1935/i/600/depositphotos_19354785-stock-photo-coffee.jpg' >
    <img vbind:src="https://media.istockphoto.com/photos/come-join-us-for-a-coffee-picture-id1150956580?k=20&m=1150956580&s=612x612&w=0&h=A6xv5WT5YJtj-9eGHL17MZ0DFDIXjAZQbzVBGjYB7R0=" >
    <img src="falls2.jpg">
    <img src="paris.jpg">
    <img src="nature.jpg">
    <img src="mist.jpg">
    <img src="paris.jpg">
  </div>
  <div class="column">
    <img src="underwater.jpg">
    <img src="ocean.jpg">
    <img src="wedding.jpg">
    <img src="mountainskies.jpg">
    <img src="rocks.jpg">
    <img src="underwater.jpg">
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