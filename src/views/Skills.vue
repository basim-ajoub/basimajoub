<template>
    <div class="skills-view">
   <div class="title">
      <h1>Skills</h1>
      <h3>My Strengths</h3>
    </div>
    <div class="skill-comp">
      <SkillsComp />
    </div>
    <div class="moving-skills">
        <div class="circle-div">
        <div class="skill skill-1">
          <span> HTML</span> 
        </div>
         <div class="skill skill-2">
          <span> CSS</span> 
        </div>
         <div class="skill skill-3">
          <span> Java Scripts</span> 
        </div>
        
         <div class="skill skill-4">
          <span> Python</span> 
        </div>
         <div class="skill skill-5">
          <span> JQuery</span> 
        </div>
         <div class="skill skill-6">
          <span> SASS</span> 
        </div>
         <div class="skill skill-7">
          <span> Vue.JS</span> 
        </div>
    </div>
    </div>
    </div>
</template>
<script>
import SkillsComp from "../components/skillsComp.vue"
export default {
    name:"skills",
    components:{
      SkillsComp
    },
}
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
.skills-view{
     .title {
      h3 {
          left: 40%;
      }
   
    }
    .moving-skills{
        width: 50%;
        height: 450px;
        z-index: 30;
        margin-left: 60%;
        font-family: $meriendaFont;
        text-shadow: -2px 1px 0px $blackCol;
        font-size: 15px;
        .circle-div{
            width: 60%;
            height: 100%;
            margin-left: 20%;
           // background: yellow;
            border-radius: 100%;
           position: relative;
        .skill{
            width: 100px;
            height: 30px;
           // background: green;
            margin: 1px;
            position: absolute;
            text-align: left;
            font-weight: bold;
            color: aliceblue;
            opacity: 0.1;
        }
        .skill-1{
            left: 50%;
            top:0px;
            animation-name: skill-1;
            animation-delay: 0.2s;
            animation-fill-mode: both;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            @keyframes skill-1 {
                0%{left: 50%;}
                25%{left: 25%; top: 392px;}
                50%{left: 0%;top: 200px;}
                75%{left: 75%;top: 350px;}
                 100%{left: 12%; top: 75px;}
            }
        }
          .skill-2{
            left: 50%;
            top:0px;
            animation-name: skill-2;
            animation-delay: 0.2s;
            animation-fill-mode: both;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            @keyframes skill-2 {
                0%{left: 12%; top: 75px;}
                  25%{left: 75%;top: 350px;}
                 50%{left: 50%;top: 0px;}
                 75%{left: 25%; top: 392px;}
                100%{left: 50%;}
                
                
              
            }
        }
        .skill-3{
            left: 80%;
            top:200px;
            animation-name: skill-3;
            animation-delay: 0.2s;
            animation-fill-mode: both;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            @keyframes skill-3 {
                0%{left: 80%; top: 200px;}
                     25%{left: 45%; top: 152px;}
                       50%{left: 13%;top: 350px;}
                75%{left: 45%;top:415px ;}

                  100%{left: 73%;top: 350px;}
               
            
                
                
              
            }
        }
         .skill-4{
            left: 80%;
            top:200px;
            animation-name: skill-4;
            animation-delay: 0.2s;
            animation-fill-mode: both;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            @keyframes skill-4 {
               
                    0%{left: 73%;top: 350px;}
                       25%{left: 13%;top: 150px;}
                         50%{left: 45%; top: 152px;}
                75%{left: 25%;top:15px ;} 
                100%{left: 80%; top: 200px;}

                 
               
            
                
                
              
            }
        }
        .skill-5{
            left: 15%;
            top:75%;
            animation-name: skill-5;
            animation-delay: 0.2s;
            animation-fill-mode: both;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            @keyframes skill-5 {
                0%{left: 15%; top: 75%;}
                  25%{left: 75%;top: 2%;}
                 50%{left: 75%;top: 72%;}
                 75%{left: 5%; top: 50%;}
                100%{left: 50%; top: 50%;}
                
                
              
            }
        }
         .skill-6{
            left: 50%;
            top:50%;
            animation-name: skill-6;
            animation-delay: 0.2s;
            animation-fill-mode: both;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            @keyframes skill-6 {
                0%{left: 50%; top: 50%;}
                  25%{left: 15%;top: 10%;}
                 50%{left: 80%;top: 35%;}
                 75%{left: 55%; top: 5%;}
                100%{left: 15%; top: 80%;}
                
                
              
            }
        }
            .skill-7{
            left: 20%;
            top:60%;
            animation-name: skill-7;
            animation-delay: 0.2s;
            animation-fill-mode: both;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            @keyframes skill-7 {
                0%{left: 20%; top: 60%;}
                  25%{left: 50%;top: 80%;}
                 50%{left: 35%;top: 40%;}
                 75%{left: 65%; top: 20%;}
                100%{left: 20%; top: 60%;}
                
                
              
            }
        }
        }
    }
}
@media only screen and (min-width: 575px) and (max-width: 850px) {
  .title {
    margin-bottom: 0px;
    h1{
      left: 35%;
    }
   
  }
  .skills-view .title  h3{
      left: 27%;
    }
}
@media only screen  and (max-width: 700px) {
.skills-view .moving-skills{
  width: 100%;
  margin-left: 0%;
}
.skills-comp{
  width: 85%;
  ul{
    font-size: 14px;
        .details-title{
          font-size: 15px;
        }
  }
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
   .skills-view .title  h3{
      left: 16%;
      top: 42px;
      letter-spacing: 6px;
      font-size: 30px;
    }
}
</style>