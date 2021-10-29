<template>
  <div class="box">
    
    <div id="testtextchange" class="project-box">
      <img :src="mainheaderimg" alt="" />
     
      <div class="hover-box">
         <h5>{{mainname}}</h5>
        <button @click="showSingleProject"  id="view-btn"> View</button>
        
      </div>
    </div>
    
  </div>
</template>
<script>
export default {
  name: "projectBox",
  props:["mainname","mainurl","mainimgnumber","mainheaderimg","maintype"],
    methods:{
 
    showSingleProject:function(){
      document.getElementById("all-projects-box").style.display = "none";
      document.getElementById("view-single-project-box").style.display = "block";
      document.getElementById("back-icon").style.display = "block";
       document.getElementById("view-img").src = this.mainheaderimg;
       document.getElementById("view-name").innerText = this.mainname;
         document.getElementById("view-type").innerText = this.maintype;
        document.getElementById("view-url").innerText = this.mainurl;
        document.getElementById("img-current-number").innerText = 1;
        document.getElementById("img-number-span").innerText = this.mainimgnumber;
    },

     changeImgLeft:function(){},
  },
};
</script>
<style lang="scss">
$permanentFont: "Permanent Marker", cursive;
$kashenFont: "Kaushan Script", cursive;
$meriendaFont: "Merienda", cursive;
$luckiestFont: "Luckiest Guy", cursive;
$yellowCol:rgb(230, 173, 67);
$blackOpCol:rgba(0, 0, 0, 0.863);
$whiteCol:rgba(233, 233, 233, 0.781);
$blackCol:rgb(0, 0, 0);
.project-box {
  width: 300px;
  height: 200px;
  position: relative;
  margin: 17px;
  margin-bottom: 25px;
  margin-left: 4%;
  border-radius: 2%;
  // background: rgb(255, 255, 255);
  .hover-box{
    width: 100%;
    height: 200px;
    font-family: $meriendaFont;
    letter-spacing: 1px;
        background: $yellowCol;
      background: linear-gradient(
        221deg,
        rgba(230, 173, 67, 0.918) 7%,
        rgba(173, 143, 36, 0.918) 97%,
        rgba(214, 162, 93, 0.918) 100%
      );
    opacity: 0;
    position: absolute;
    z-index: 20;
    top: 0;
     border-radius: 2%;
    transition: all 0.4s ease-in-out;
#view-btn{
margin-top: 120px;
width: 25%;
height: 30px;
background: $blackCol;
border: 1px solid $whiteCol;
border-radius: 15%;
color: $whiteCol;
}
  }
  h5 {
    position: absolute;
    top: 20px;
    z-index: -1;
    width: 100%;
    font-weight: bolder;
  }
  cursor: pointer;
  float: left;
  img {
    width: 300px;
    height: 200px;
    border-radius: 2%;
    box-shadow: 0px 1px 7px rgba(209, 198, 179, 0.76);
    transition: all 0.4s ease-in-out;
    z-index: 1;
  }
  &:hover {
    transform: translateY(5px);
 

      box-shadow: 0px 1px 7px rgba(230, 173, 67, 0.76);
.hover-box{
opacity: 1;

}
    h5 {
      z-index: 4;
      color: black;
    }

    &:active {
      cursor: wait;
    }
  }
}
@media screen and (max-width:575px) {
  .all-projects-comp{
height: 2500px;
  }
  .project-box {
      transform: translateY(0px);

height: 325px;
  .hover-box {
position: initial;
  
    opacity: 1;
    top: 200px;
    height: 100px;
   
background: rgba(226, 0, 0, 0);
h5{
  position: initial;
  margin-top: 20px;
  color: $yellowCol;
}
#view-btn{
margin-top: 120px;
width: 25%;
height: 30px;
background: black;
border: 1px solid wheat;
border-radius: 15%;
color: wheat;
margin-top: 20px;
}
&:hover{
  background: rgba(0, 0, 0, 0);
}
  }}
}
</style>
