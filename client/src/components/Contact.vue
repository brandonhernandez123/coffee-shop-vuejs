<template>
    <b-container fluid>
       
 <div class="wrapper">
    <form class="form">
      <div class="pageTitle title">Contact Us! </div>
      <div class="secondaryTitle title">Please fill this form to reach out to us!</div>
      <input type="text" class="name formEntry" placeholder="Name" />
      <input type="text" class="email formEntry" placeholder="Email"/>
      <textarea class="message formEntry" placeholder="Message"></textarea>
      <button class="submit formEntry">Submit</button>
    </form>
  </div>
            
      

    
      
    
   
    </b-container>
</template>

<script>
export default {
    name: 'ContactForm'
}
</script>

<style>


#title-Tag-Line {
  font-size: 20px;
}
/* .card-item__bg{
  width: 150px;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  display: block;
  position: relative;
  margin: 30px auto;
  transform: translate(0px, 50px);
  z-index: 5;
} */

/* form animation starts */
.form {
  background: #8A624A;
  box-shadow: 0 30px 60px 0 rgba(90, 116, 148, 0.4);
  border-radius: 5px;
  max-width: 450px;
  margin: 0 auto;
  padding-top: 5px;
  padding-bottom: 5px;
  left: 0;
  right: 0;
  /* position: absolute; */
  border-top: 8px solid tan;
  border-right: 8px solid tan;
  border-left: 8px solid tan;
  border-bottom: 8px solid tan;
/*   z-index: 1; */
  animation: bounce 1.5s infinite;
}
::-webkit-input-placeholder {
  font-size: 1.3em;
}

.title{
  display: block;
 
  margin: 10px auto 5px;
  width: 300px;
}
.termsConditions{
  margin: 0 auto 5px 80px;
}

.pageTitle{
  font-size: 2em;
  font-weight: bold;
}
.secondaryTitle{
  color: grey;
}

.name {
  background-color: black;
  color: white;
}
.name:hover {
  border-bottom: 5px solid tan;
  height: 30px;
  width: 380px;
  transition: ease 0.5s;
}

.email {
  background-color: black;
  color: white;
  height: 2em;
}

.email:hover {
  border-bottom: 5px solid tan;
  height: 30px;
  width: 380px;
  transition: ease 0.5s;
}

.message {
  background-color: black;
  color: white;
  overflow: hidden;
  height: 10rem;
  max-width: 250px;
}

.message:hover {
  border-bottom: 5px solid tan;
  height: 12em;
  width: 380px;
  transition: ease 0.5s;
}

.formEntry {
  display: block;
  margin: 30px auto;
  min-width: 300px;
  padding: 10px;
  border-radius: 2px;
  border: none;
  transition: all 0.5s ease 0s;
}

.submit {
  width: 200px;
  color: white;
  background-color: tan;
  font-size: 20px;
}

.submit:hover {
  box-shadow: 15px 15px 15px 5px rgba(78, 72, 77, 0.219);
  transform: translateY(-3px);
  width: 300px;
  border-top: 5px solid #0e3750;
  border-radius: 0%;
}

@keyframes bounce {
  0% {
    tranform: translate(0, 4px);
  }
  50% {
    transform: translate(0, 8px);
  }
} 


</style>

