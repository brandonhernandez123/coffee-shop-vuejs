<template>
    <div>
        <b-container fluid class="about">
            <h2 id="abouttitle">About Us!</h2>
  <b-row class="aboutrow">
    <b-col lg='7' >
        <b-img fluid id="aboutimg" height="400" width="500" src="https://images.unsplash.com/photo-1554118811-1e0d58224f24?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTh8fGNvZmZlZSUyMHNob3B8ZW58MHx8MHx8&w=1000&q=80" />
    </b-col>
    <b-col lg='4'  id="aboutcol" >
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Nunc faucibus a pellentesque sit amet porttitor eget dolor. Dolor sed viverra ipsum nunc aliquet bibendum. Purus semper eget duis at tellus at urna condimentum. Sapien et ligula ullamcorper malesuada proin libero nunc. Maecenas sed enim ut sem viverra aliquet eget sit. Aliquam sem fringilla ut morbi tincidunt augue interdum velit euismod. Nec feugiat nisl pretium fusce. Diam sollicitudin tempor id eu nisl nunc mi ipsum faucibus. Sapien nec sagittis aliquam malesuada bibendum. Elementum sagittis vitae et leo duis ut diam quam nulla. Sed lectus vestibulum mattis ullamcorper velit sed ullamcorper morbi. Pulvinar etiam non quam lacus suspendisse faucibus interdum posuere lorem. Scelerisque eleifend donec pretium vulputate. Egestas diam in arcu cursus. Interdum consectetur libero id faucibus nisl tincidunt eget. Libero enim sed faucibus turpis in.

    </b-col>
   
  </b-row>
</b-container>


    </div>
</template>


<script>
export default {
    name: 'AboutUs'
}
</script>

<style>
    .about{
        height: max-content;
        background-color: bisque;
    }

    #abouttitle{
        margin-top: 40px;
        text-decoration-line: underline;
    }

    .aboutrow{
        margin-top: 100px;
    }

    @media screen and (max-width: 600px) {
        #aboutimg{
            width: 350px;
        }
    }

    #aboutcol{
        margin-top: 40px;
        font-stretch: semi-condensed;
        background-color: blanchedalmond;
        
    }

   
</style>