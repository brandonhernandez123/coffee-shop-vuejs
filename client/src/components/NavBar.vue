<template>
    
<div class="sidebar">
  <a class="active" href="#home">Coffee Shop</a>
  <a href="#about">About</a>
  <a href="#gallery">Gallery</a>
  <a href="#menu">Menu</a>
</div>

</template>


<script>
export default {
    name: 'NavBar'
}
</script>


<style>
.sidebar {
  margin: 0;
  padding: 0;
  width: 200px;
background-color: #fbeec1;  position: fixed;
  height: 100%;
  overflow: auto;
}

.sidebar a {
  display: block;
  color: black;
  padding: 16px;
  text-decoration: none;
}

.sidebar a.active {
  background-color: rgb(84, 46, 46);
  color: white;
}

.sidebar a:hover:not(.active) {
  background-color: blanchedalmond;
  color: brown;
  text-decoration-line: underline;

}


@media screen and (max-width: 700px) {
  .sidebar {
    width: 100%;
    height: auto;
    position: relative;
  }
  .sidebar a {float: left;}
  div.content {margin-left: 0;}
}

@media screen and (max-width: 300px) {
  .sidebar a {
    text-align: center;
    float: none;
  }
}

</style>

