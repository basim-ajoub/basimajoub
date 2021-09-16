<template>
  <div class="all-projects-comp">
    <div class="title">
      <h1>Projects</h1>
      <h3>My Works</h3>
    <p id="back-icon" class="back-icon"> <fontawesome-icon class="icon" @click="backClick"  :icon="['fas', 'arrow-left']" />All Projects</p> 
    </div>
    
    <div id="all-projects-box" class="all-projects-box" >
      <SingleProject v-for="project in projects" :key="project.id"  :mainname="project.name" :maintype="project.type" :mainheaderimg="project.headerimg" :mainimgnumber="project.imgnumber" :mainurl="project.url" />
    </div>
        <div id="view-single-project-box" class="view-single-project-box">
       <div class="view-project row">
<div class="projects-images col-ms-6">
        <fontawesome-icon @click="changeImgRight" id="click-right-btn" class="change-img click-right" :icon="['fas', 'arrow-circle-right']"/>
   
    <img id="view-img" src="project-5.png" alt="" />
     <fontawesome-icon @click="changeImgLeft"  id="click-left-btn"  class="change-img click-left" :icon="['fas', 'arrow-circle-left']"/>
 <span id="counter" class="counter"> <span id="img-current-number" class="img-current-number"></span> / <span id="img-number-span" class="img-number-span"></span> </span>
</div>
<div class="projects-disc col-md-6">
    <ul class="row">
   <li> <p  class="main-details ">Name :</p> <span id="view-name" class="details" ></span></li>
   <li> <p class="main-details ">Type :</p> <span id="view-type"  class="details "> Mangement System</span></li>
  <li>  <p class="main-details ">Url :</p> <a id="view-url"  class="details " href="#"> www.storemanagmentsystem.com</a></li>
</ul>
</div>

    </div>
    </div>
  </div>
</template>
<script>
import SingleProject from "./projectBoxComp.vue";

import allJsonProjects from "../../json/projects.json";
export default {
  name: "allProjectsCom",

  components: {
    SingleProject,
    
 
  },
  data:function(){
    return{
    projects:allJsonProjects,
    }
  },
  methods:{
backClick:function(){
      document.getElementById("all-projects-box").style.display = "block";
      document.getElementById("view-single-project-box").style.display = "none";
      document.getElementById("back-icon").style.display = "none";
},
        changeImgRight:function(){
     var srcimg = document.getElementById("view-img").src;
     var splitSrcImg = srcimg.split("-");//background , 3 , 1 we need number 3
var oldimg = splitSrcImg[2].split(".");//4.png we need tosplit .png ang get the number then conver it to integer from string

var intOldImg = Number(oldimg[0]);//img number to change
var x = document.getElementById("img-number-span").innerText;
 x = Number(x);
  var counter = document.getElementById("img-current-number").innerText;
 counter = Number(counter); 
if(counter >= 1 && counter < x){
document.getElementById("click-right-btn").style.opacity = "1";
document.getElementById("click-left-btn").style.opacity = "1";
  counter ++;
  var newImgNumber =  intOldImg + 1;

    var newImgScr = "project-"+splitSrcImg[1]+"-"+newImgNumber+".png";
    document.getElementById("view-img").src = newImgScr;
  
  


  if(counter == x){
      document.getElementById("click-right-btn").style.opacity = "0.5";
  }
  document.getElementById("img-current-number").innerText = counter;
 
  console.log(newImgScr)
}
else{
  document.getElementById("click-right-btn").style.opacity = "0.5";
}



    },
  changeImgLeft:function(){
       var srcimg = document.getElementById("view-img").src;
     var splitSrcImg = srcimg.split("-");//background , 3 , 1 we need number 3
var oldimg = splitSrcImg[2].split(".");//4.png we need tosplit .png ang get the number then conver it to integer from string

var intOldImg = Number(oldimg[0]);//img number to change
var x = document.getElementById("img-number-span").innerText;
 x = Number(x);
  var counter = document.getElementById("img-current-number").innerText;
 counter = Number(counter);
if(counter > 1 && counter <= x){
document.getElementById("click-left-btn").style.opacity = "1";
document.getElementById("click-right-btn").style.opacity = "1";

  var newImgNumber =  intOldImg - 1;

    var newImgScr = "project-"+splitSrcImg[1]+"-"+newImgNumber+".png";
    document.getElementById("view-img").src = newImgScr;
  
    if(counter == 2){
        counter --;
      document.getElementById("click-left-btn").style.opacity = "0.5";
  }
  else{
    counter --;
  }

    
  document.getElementById("img-current-number").innerText = counter;
  console.log(counter)
}
else{
  document.getElementById("click-left-btn").style.opacity = "0.5";
}



    },
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
.all-projects-comp {
  .title {
    h1 {
      left: 37%;
    }
    .back-icon{
      position: absolute;
      display: none;
     top: 115px;
     cursor: pointer;
     left: 5%;
     font-size: 10px;
     color: $yellowCol;
     letter-spacing: 0.5px;
     font-family:$meriendaFont ;
     .icon{
       font-size: 22px;
       
     }
    }
  }
  .all-projects-box {
      width: 100%;
      height: 480px;
      overflow: hidden;

  }
.view-single-project-box{
 width: 100%;
 height: 460px;
 display: none;
 
  .view-project{
    width: 100%;
    height: 455px;
  // background: wheat;
 overflow: hidden;
    .projects-disc{
        width: 25%;  
        height: 100%;
        padding-left: 0;
        ul{
            margin-top: 120px;
            list-style-type: none;
            overflow: hidden;
            font-size: 14px;
            text-align: left;
            margin-left: -10%;
            letter-spacing: 2px;
            color:$yellowCol;
            font-family: $meriendaFont;
            li{
                margin-bottom: 30px;
                letter-spacing: 0.8px;
                span ,a{
font-weight: bolder;
color: rgb(233, 233, 233);
font-family: $kashenFont;
                }
            p{
                font-size: 16px;
            }
            a{
            font-size: 12px;
            }
            }
        }
    }
    .projects-images{
        width: 75%;
        height: 100%;
        position: relative;
        overflow: hidden;
       
        img{
            width: 100%;
            height: 100%;
            border-radius: 1%;
        }
        .change-img{
            width: 3%;
            height: 27px;
            position: absolute;
             top: 47%;
                         color:$yellowCol;
background: $blackCol;
font-size: 17px;
border-radius: 100%;
cursor: pointer;
        }
        .click-right{
            right: 1.6%;
           
        }
         .click-left{
            left: 1.6%;
           
        }
        #counter{
          position: absolute;
          width: 10%;
          height: 20px;
          width: 15%;
          font-size: 14px;
          background: $yellowCol;
          border-radius: 10%;
          bottom: 0;
          left: 45%;
          font-family: $kashenFont;
        }

    }
}
}
}

//PC Screen Setting
@media only screen and (min-width: 571px) and (max-width: 1195px) {
.project-box{
   width: 30%;
  height: 160px;
margin: 0;
margin-bottom: 50px;
z-index:98;
margin-left: 3%;
.hover-box{
  height: 160px;
}
h5{
  font-size: 17.5px;
}
   img{
 width: 100%;
  height: 160px;
}
}

}
//view window 
@media only screen and  (max-width: 800px) {
  
.all-projects-comp .view-single-project-box{
  height: 1100px;
  .view-project{
    height: 1100px;
    .projects-images{
     height: 400px;
  width: 100%;
   .change-img{
     width: 6%;
     cursor: pointer;
   }
  img{
    height: 400px;
    width: 100%;
  }
}}}
.all-projects-comp .view-single-project-box .view-project .projects-disc{
  width: 100%;
  ul{
    margin-left: 0;
  }
}
}

//mobile screen setting
@media only screen and (max-width: 570px){
  .all-projects-comp .all-projects-box{
    height: 2500px;
    padding-left: 8%;
  }
  .all-projects-comp .title h1{
      left: 12%;
    }
    h3{
      left: 25.8%;
    }
  
  #app {
    height: 2500px;
  }
}
@media only screen  and (max-width: 570px) {
.title {
  
    margin-bottom: 110px;
    h1{
      left: 25%;
      top: -27px;
      font-size: 50px ;
    }
   
  }
}
</style>
