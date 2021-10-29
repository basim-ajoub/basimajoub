<template>
  <div id="app">
     <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap"
      rel="stylesheet"
    />
    <link
      href="https://fonts.googleapis.com/css2?family=Kaushan+Script&display=swap"
      rel="stylesheet"
    />
    <link
      href="https://fonts.googleapis.com/css2?family=Merienda&display=swap"
      rel="stylesheet"
    />
    <link
      href="https://fonts.googleapis.com/css2?family=Luckiest+Guy&display=swap"
      rel="stylesheet"
    />
    <div id="nav">
      <ul class="nav-list">
        <li class="list-element">
          <router-link to="/"
            ><fontawesome-icon class="contact-icon" :icon="['fas', 'home']" />
            <p class="icon-disc">Home</p></router-link
          >
        </li>
        <li class="list-element">
          <router-link to="/about"
            ><fontawesome-icon
              class="contact-icon"
              :icon="['fas', 'address-card']"
            />
            <p class="icon-disc">About</p></router-link
          >
        </li>
                <li class="list-element">
          <router-link to="/skills"
            ><fontawesome-icon
              class="contact-icon"
              :icon="['fas', 'chalkboard-teacher']"
            />
            <p class="icon-disc">Skills</p></router-link
          >
        </li>
        <li class="list-element">
          <router-link to="/projects"
            ><fontawesome-icon class="contact-icon" :icon="['fas', 'laptop-code']" />
            <p class="icon-disc">Projects</p></router-link
          >
        </li>
        <li class="list-element">
          <router-link to="/contact"
            ><fontawesome-icon
              class="contact-icon"
              :icon="['fas', 'comments']"
            />
            <p class="icon-disc">Contact</p></router-link
          >
        </li>
        <li class="list-element">
          <router-link to="/resume"
            ><fontawesome-icon class="contact-icon" :icon="['fas', 'file-pdf']" />
            <p class="icon-disc">Resume</p></router-link
          >
        </li>
      </ul>
    </div>
    <div class="container">
      <router-view />
    </div>
    <div id="mobile-drop-meue" class="mobile-drop-meue">
      <div
        @click="showHideDropMenue"
        id="mobile-drop-btn"
        class="mobile-drop-btn"
      >
        <button id="drop-btn" class="drop-btn">
          <fontawesome-icon
            id="btn-icon"
            class="btn-icon"
            :icon="['fas', 'bars']"
          />
        </button>
      </div>
      <div id="mob-list-drop" class="mob-list-drop">
        <ul class="nav-list">
          <li class="list-element">
            <router-link to="/"
              ><fontawesome-icon class="contact-icon" :icon="['fas', 'home']" />
              <p class="icon-disc">Home</p></router-link
            >
          </li>
          <li class="list-element">
            <router-link to="/about"
              ><fontawesome-icon
                class="contact-icon"
                :icon="['fas', 'address-card']"
              />
              <p class="icon-disc">About</p></router-link
            >
          </li>
            <li class="list-element">
          <router-link to="/skills"
            ><fontawesome-icon
              class="contact-icon"
              :icon="['fas', 'chalkboard-teacher']"
            />
            <p class="icon-disc">Skills</p></router-link
          >
        </li>
          <li class="list-element">
            <router-link to="/projects"
              ><fontawesome-icon class="contact-icon" :icon="['fas', 'laptop-code']" />
              <p class="icon-disc">Projects</p></router-link
            >
          </li>
          <li class="list-element">
            <router-link to="/contact"
              ><fontawesome-icon
                class="contact-icon"
                :icon="['fas', 'comments']"
              />
              <p class="icon-disc">Contact</p></router-link
            >
          </li>
          <li class="list-element">
            <router-link to="/resume"
              ><fontawesome-icon class="contact-icon" :icon="['fas', 'file-pdf']" />
              <p class="icon-disc">Resume</p></router-link
            >
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "app",
  methods: {
    showHideDropMenue: function () {
      var x = document.getElementById("mob-list-drop").style.display;
      if (x == "block") {
        document.getElementById("mob-list-drop").style.display = "none";
        document.getElementById("mobile-drop-meue").style.height = "0px" ;
        document.getElementById("drop-btn").style.background =
          "rgb(230, 173, 67)";
        document.getElementById("drop-btn").style.border =
          "1px solid $whiteCol";
        document.getElementById("btn-icon").style.color =
          "rgba(0, 0, 0, 0.925)";
      } else {
        document.getElementById("mob-list-drop").style.display = "block";
        document.getElementById("mobile-drop-meue").style.height = "200px" ;
        document.getElementById("drop-btn").style.background =
          "rgba(0, 0, 0, 0.925)";
        document.getElementById("drop-btn").style.border =
          "2px solid $whiteCol";
        document.getElementById("btn-icon").style.color = "rgb(230, 173, 67)";
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
* {
  padding: 0;
  margin: 0;

 

  h1 {
    color: $yellowCol;
  }
  a {
    color: $blackOpCol;
  }
  .title {
    position: relative;
    width: 100%;
    height: 90px;
    margin-bottom: 60px;

    h1,
    h3 {
    
      position: absolute;
      color: $yellowCol;
    }
    h3 {
      left: 42.8%;
      top: 35px;
      font-weight: bold;
      font-size: 35px;
font-family: $kashenFont;
      letter-spacing: 8px;
    }
    h1 {
      font-family: $permanentFont;
      letter-spacing: 10px;
      top: -50px;
      left: 42%;
      font-size: 60px;
      opacity: 0.15;
      font-weight: 850;
      color: $whiteCol;
    }
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: inline-flex;
  background: $blackCol;
  background: linear-gradient(
    221deg,
    rgba(0, 0, 0, 1) 50%,
    rgba(0, 0, 0, 0.9920167896260067) 97%,
    rgb(37, 35, 35) 100%
  );
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.container {
  width: 92%;
  height: 100%;
  //background: red;
}
#nav {
  width: 7%;
  height: 643px;
  z-index: 16;
  border-top-right-radius: 20%;
  border-bottom-right-radius: 20%;
  //background: rgba(235, 235, 235, 0.89) ;
  background: $yellowCol;
  background: linear-gradient(
    221deg,
    rgba(230, 173, 67, 1) 7%,
    rgba(173, 144, 36, 0.9920167896260067) 97%,
    rgba(232, 169, 86, 1) 100%
  );
  a {
    font-weight: bold;
    color: $blackOpCol;
    text-decoration: none;
    font-size: 25px;

    &.router-link-exact-active {
      transition: all 0.4s ease-in-out;
      color: rgba(235, 235, 235, 0.89);
      .contact-icon {
        float: left;
        animation-name: showElement;

        animation-delay: 0.2s;
        animation-duration: 0.4s;
        animation-iteration-count: 1;
        animation-fill-mode: forwards;
        @keyframes showElement {
          0% {
            font-size: 23px;
          }
          25% {
            font-size: 22px;
          }
          50% {
            font-size: 21px;
          }
          75% {
            font-size: 20px;
          }
          100% {
            font-size: 18px;
            margin-left: 5px;
          }
        }
      }
      .icon-disc {
        display: block;
        margin-left: 120%;
        animation-name: showDisc;
        animation-delay: 0.4s;
        animation-duration: 0.2s;
        animation-iteration-count: 1;
        animation-fill-mode: forwards;
        @keyframes showDisc {
          0% {
            margin-left: 120%;
          }
          50% {
            margin-left: 75%;
          }
          100% {
            margin-left: 0%;
          }
        }
      }
    }
  }
}
.nav-list {
  //background: red;
  width: 90%;
  list-style: none;
  padding-left: 0px;
  margin-top: 100px;
}
.list-element {
  width: 100%;
  margin-top: 50px;
  overflow: hidden;
  transition: all 0.4s ease-in-out;
}
.icon-disc {
  font-size: 10px;
  display: none;
  font-weight: bolder;
     font-family: $meriendaFont;
     letter-spacing: 2px;
}
a {
  font-weight: bold;
  color: $blackOpCol;
  text-decoration: none;
  font-size: 25px;

  &.router-link-exact-active {
    transition: all 0.4s ease-in-out;
    color: $whiteCol;
  }
}
.mobile-drop-meue {
  width: 100%;
  height: 100%;

  position: absolute;
  top: 0;
  left: 0;
  display: none;
  .mobile-drop-btn {
    position: absolute;
    right: 3%;
    top: 30px;
    z-index: 100;
    width: 7%;

    #drop-btn {
      width: 100%;
      height: 30px;
      background: $yellowCol;
      border: 1px solid $whiteCol;
      border-radius: 5%;
    }
    .btn-icon {
      width: 100%;

      color: rgba(0, 0, 0, 0.925);
    }
  }
  .mob-list-drop {
    position: absolute;
    position: fixed;
    width: 100%;
    height: 100%;
   
    background: $yellowCol;
    background: linear-gradient(
      221deg,
      rgba(230, 173, 67, 1) 7%,
      rgba(173, 144, 36, 0.9920167896260067) 97%,
      rgba(232, 169, 86, 1) 100%
    );
    z-index: 99;
    display: none;
   .list-element{
  
    a {
    
  color: $blackOpCol;
  text-decoration: none;
  font-size: 40px;
  width: 100%;
 
  text-align: center;
  
.contact-icon{
  float: left;
  margin-left: 30%;
}
  &.router-link-exact-active {
    transition: all 0.4s ease-in-out;
    color: $whiteCol;
  }
  .icon-disc {
  display: block;
  font-size: 25px;
      width: 85%;
    margin-top: 4px;
   font-family: $meriendaFont;
     letter-spacing: 2px;
     font-weight: 1000;
    
}
  
}
   }
  }
}
@media only screen and (min-height: 645px) {
  #nav {
    height: 657px;
  }
}
@media only screen and (max-width: 575px) {
  #nav {
    display: none;
  }
  .mobile-drop-meue {
    display: block;
    height: 0px ;
   
  }
  .container {
    width: 100%;
    padding-left: 0;
    padding-right: 0;
  }
}
@media only screen and (max-width: 570px) {
  * {
    .title {
      h3 {
        left: 19%;
        top: 42px;
      }
      h1 {
        top: -40px;

        left: 25%;
      }
    }
  }
  #app {
    height: 1650px;
  }
}
</style>
