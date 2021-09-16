<template>
  <div class="home">
    <div id="component" class="component row">
      <div id="header-box" class="header-box col-md-7">
        <h1 class="first-header">I'm <span>B</span>asim <span>A</span>joub</h1>
        <h1>Front End Engineer</h1>
      </div>
      <div id="img-box" class="img-box col-md-5">
        <div class="img-background">
          <div class="background-2"></div>
        </div>
        <div class="img">
          <img src="basim-pic.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {},
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
.home {
  width: 100%;
  height: 100%;

  #component {
    width: 100%;
    height: 643px;

    //  background: yellow;
    .header-box {
      width: 47%;
      height: 400px;
      margin-top: 120px;
      text-align: left;
      margin-left: 3%;
      z-index: 5;
      animation-name: movingBox;
      animation-duration: 2.5s;
      animation-iteration-count: 1;
      animation-delay: 0.4s;
      animation-direction: forwards;
      transition: 0.4s ease-in-out;
      @keyframes movingBox {
        0% {
          margin-left: -68%;
        }
        35% {
          margin-left: -68%;
        }
        100% {
          margin-left: 3%;
        }
      }
      .first-header {
        margin-top: 80px;
      }
      h1 {
        margin-left: 10%;
font-family: $permanentFont;
        color: rgba(235, 235, 235, 0.89);
        word-spacing: 7px;
        letter-spacing: 5px;
        font-size: 35px;
        font-weight: bold;
        color: $yellowCol;
        text-shadow: -1px 1px 0px rgba(235, 235, 235, 0.534);

        span {
            font-family: $luckiestFont;
          //color: rgb(207, 32, 32);
          color: $yellowCol;
          font-size: 75px;
          letter-spacing: 8px;
          font-weight: 30;
          //text-shadow: -7px -1px 0px rgba(245, 62, 62 ,0.87);
          text-shadow: -6px 0px 0px rgba(235, 235, 235, 0.89);
          //Start Typing Animatin
          animation-name: typing;
          animation-delay: 4s;
          animation-iteration-count: infinite;
          animation-fill-mode: both;
          animation-direction: alternate;
          transition: 0.4s ease-in-out;
          @keyframes typing {
            0% {
              transform: translateY(0px);
            }
            100% {
              transform: translateY(2px);
            }
          }
        }
      }
    }
    .img-box {
      width: 47%;
      height: 400px;
      margin-top: 120px;
      position: relative;
      margin-left: 3%;
      animation-name: movingImg;
      animation-direction: alternate;
      animation-delay: 2.1s;
      animation-fill-mode: both;
      animation-duration: 1.5s;
      animation-iteration-count: 1;
      @keyframes movingImg {
        0% {
          transform: rotate(0deg);
        }
        50% {
          transform: rotate(45deg);
        }
        100% {
          transform: rotate(0deg);
        }
      }
      .img-background {
        width: 100%;
        position: relative;
        height: 395px;

        .background-2 {
          position: absolute;
          width: 70%;
          height: 320px;
          //   border-radius: 100%;
          border-top-left-radius: 100%;
          border-top-right-radius: 100%;
          border-bottom-right-radius: 50%;
          border-bottom-left-radius: 50%;
          //  background: rgb(235, 235, 235);
        }
        .background-2 {
          width: 50%;
          height: 299.5px;
          margin-top: 12.5px;
          margin-left: 29%;
          z-index: 4;
          //background: rgba(245, 62, 62, 0.788);
          background: rgb(230, 173, 67);
          background: linear-gradient(
            221deg,
            rgba(230, 173, 67, 1) 7%,
            rgba(173, 144, 36, 0.9920167896260067) 97%,
            rgba(232, 169, 86, 1) 100%
          );
        }
      }
      .img {
        position: absolute;
        width: 48%;
        height: 307px;
        z-index: 5;
        border-bottom-right-radius: 25%;
        border-bottom-left-radius: 24%;

        //  border-radius: 37%;
        //background: red;
        top: 5.5px;
        left: 30%;

        overflow: hidden;
        img {
          z-index: 5;
          width: 130%;
          height: 281px;
          margin-top: 27px;
          margin-left: -11%;
        }
      }
    }
  }
}
@media only screen and (min-height: 645px) {
  #component {
    width: 100%;
    height: 654px;
    margin-top: 10px;
  }
}
@media only screen and (max-width: 1204px) {
  .home #component .header-box h1 {
    margin-left: 0%;
    font-size: 27px;
    letter-spacing: 4px;
    span {
      font-size: 40px;
      text-shadow: -3px 0px 0px rgba(235, 235, 235, 0.89);
    }
  }
}
@media only screen and (max-width: 980px) {
  .home #component .header-box h1 {
    letter-spacing: 3px;
    font-size: 25px;

    span {
      font-size: 35px;
      text-shadow: -1px 0px 0px rgba(235, 235, 235, 0.89);
    }
  }
}
@media only screen and (max-width: 770px) {
  .home #component .header-box h1 {
    font-size: 18px;
    letter-spacing: 2px;
    span {
      font-size: 25px;
      text-shadow: -1px 0px 0px rgba(235, 235, 235, 0.89);
    }
  }
}
@media only screen and (max-width: 575px) {

  .home {
    #component {
      display: block;
      #header-box {
        width: 100%;
        height: 150px;
    h1{
      font-size: 28px;
      letter-spacing: 4px;
    }
    span{
      font-size:65px;
        text-shadow: -6px 0px 0px rgba(235, 235, 235, 0.89);
    }
      }
    }
  }
  .home #component .img-box .img-background .background-2{
       width: 75%;
       margin-left: 15%;
     }
   .home #component  #img-box {
       width: 100%;
          margin-left: 0;
          
          .img{
                width: 75%;
        border-bottom-right-radius: 29%;
            border-bottom-left-radius: 26%;
    left: 16%;
          }
        }
}
</style>
