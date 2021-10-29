<template>
    <div class="resume-view">
            <div class="title">
      <h1>Resume</h1>
      <h3>My CV</h3>
    </div>
    <div class="resume-container">=
<iframe src="https://drive.google.com/file/d/1_uKON2fvg0lrSAX5_G5obVNiQb-uLE2u/preview" width="640" height="470" allow="autoplay"></iframe>    </div>

    </div>
</template>
<script>
export default {
    name:"resumeView",
}
</script>
<style lang="scss">
.resume-view{

  height:640px;

    .title {
    h1 {
      left:38%;
    }
    h3 {
      left: 45%;
    }
  }
  .resume-container{
    width: 100%;
    height: 650px;
    iframe{
width: 100%;
height: 480px;
    }
  }
}
@media only screen and (max-width: 570px) {
  
   .resume-view .title{
     margin-bottom: 120px;
      h1{
      left: 13%;
      font-size: 55px;
      top: -35px;
      
     
      }
      h3 {
        left: 28%;
    
      }
    
   }
}
</style>