<template>
  <div class="about">
    <AboutComp />
  </div>
</template>
<script>
import AboutComp from "../components/aboutComp.vue"
export default {
  name:"aboutView",
  components:{
AboutComp,
  },
}
</script>
<style lang="scss">

.about{
  width: 100%;
  height: 100%;
  
}
@media only screen and (min-width: 851px) and (max-width: 980px) {
  .about-comp .about-box #disc-box ul{
  margin-top: 45px;
  }

}

@media only screen and (min-width: 575px) and (max-width: 850px) {
  .title {
    margin-bottom: 0px;
    h1{
      left: 28%;
    }
    h3{
      left: 29.8%;
    }
  }
  #img-box{
    width: 70%;
    margin-left: 20%;
    height: 300px;
  }
.about-comp .about-box #disc-box{
width: 100%;
 ul{
  margin-top: 20px;
li{
  display: block;
    
              margin-bottom: 15px;
          
  .details-title{
    font-size: 14px;
  }
  span{
    font-size: 14px;
  }
}}
}
.about-comp .about-box #disc-box p {
        letter-spacing: 0px;
    width: 100%;
    font-size: 14px;
    margin-top: 0px;
  }
}
@media only screen  and (max-width: 570px) {
  ul li{
    margin-bottom: 25px;
  }
.title {
h3{
margin-left: 5.5%;
}
}
}
</style>