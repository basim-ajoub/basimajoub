<template>
  <div class="about-comp">
    <div class="title">
      <h1>About</h1>
      <h3>About Me</h3>
    </div>

    <div class="about-box row">

   <div id="img-box"  class="part col-md-5">
            <img src="basim-pic.png" alt="">
        </div>

        <div id="disc-box"  class="part col-md-7">
            <p>Innovative Programmer and Communications Engineer striving to make the world a more unified and connected place, Able to Self-discipline & see things from various points of view, Able to understand and follow instructions  as well as committed to deadlines. </p>
        <ul>
            <li class="row"><span class="details-title col-md-4">Name:</span><span class="col-md-8">Basim Ajoub .</span></li>
             <li class="row"><span class="details-title col-md-4">Birth:</span><span class="col-md-8">October 04 .</span></li>
              <li class="row"><span class="details-title col-md-4">Degree:</span><span class="col-md-8">B.E. Electronics & Communcations Eng. .</span></li>
                       <li class="row"><span class="details-title col-md-4">University:</span><span class="col-md-8">M.S. Ramaiah College , India .</span></li>
                             <li class="row"><span class="details-title col-md-4">job:</span><span class="col-md-8">Front-End Web Engnieer .</span></li>
        </ul>
        </div>
             
    </div>
  </div>
</template>
<script>
export default {
  name: "aboutComp",
};
</script>
<style lang="scss">
$permanentFont: "Permanent Marker", cursive;
$kashenFont: "Kaushan Script", cursive;
$meriendaFont: "Merienda", cursive;
$luckiestFont: "Luckiest Guy", cursive;
$yellowCol:rgb(230, 173, 67);

.about-comp {
 
  .about-box{
     
      height: 485px;
  
#img-box{
   


    img{
        width: 100%;
        height: 90%;
    //    border-right: 1px solid $yellowCol;
    }
}
#disc-box{
   font-weight: 600;

    p{
 color:rgb(233, 233, 233) ;
 letter-spacing: 1px;
margin-top: 50px;

font-family: $meriendaFont;
    }
    text-align: left;
    ul{
        margin-top: 130px;
        letter-spacing: 2px;
  color:$yellowCol  ;
    list-style-type: none;
font-size: 15.2px;
font-family: $meriendaFont;
li{
  margin-bottom: 4px;
}
    }

 .details-title{
    letter-spacing: 0.8px;
font-weight: bolder;
color: rgb(233, 233, 233);
font-size: 17px;
font-family: $kashenFont;

 }
   
}
  }
}
</style>
