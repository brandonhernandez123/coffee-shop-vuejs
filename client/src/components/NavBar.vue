<template>
    
<div>
  <!-- Image and text -->
  <b-navbar id="nav" variant="danger" class="fixed-bottom" type="light" sticky >
    <b-navbar-brand href="/">
      <img src="https://static.vecteezy.com/system/resources/thumbnails/003/529/350/small/coffee-logo-free-vector.jpg" height="50" width="100" class="d-inline-block align-top" alt="coffee-shop">
      Coffee shop
    </b-navbar-brand>
  </b-navbar>
</div>
</template>


<script>
export default {
    name: 'NavBar'
}
</script>


<style>
#nav{
  background-color: bisque !important;
  position: sticky !important;
  
}
</style>