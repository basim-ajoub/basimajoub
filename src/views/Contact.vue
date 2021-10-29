<template>
  <div class="contact-view">
    <div class="title">
      <h1>Contacts</h1>
      <h3>Contact Method</h3>
    </div>
    <div class="contact-container row">
      <div class="contact-box col-md-7">
        <div class="informarion-box">
          <ul>
            <li class="row">
              <span class="details-title col-md-4">Email:</span
              ><span class="col-md-8">basemajoub2@gmail.com .</span>
            </li>
            <li class="row">
              <span class="details-title col-md-4">Phone:</span
<<<<<<< HEAD
              ><span class="col-md-8">+49 | 15752790114 .</span>
=======
              ><span class="col-md-8">+963 | 93556043 .</span>
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
            </li>
            <li class="row">
              <span class="details-title col-md-4">Skype:</span
              ><span class="col-md-8">b_asim_star.skypy.com .</span>
            </li>
            <li class="row">
<<<<<<< HEAD
              <span class="details-title col-md-4">Location:</span
=======
              <span class="details-title col-md-4">Address:</span
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
              ><span class="col-md-8">Berlin , Germany .</span>
            </li>
            <li class="row">
              <span class="details-title col-md-4">ZIP:</span
<<<<<<< HEAD
              ><span class="col-md-8">10365 .</span>
=======
              ><span class="col-md-8">100505 .</span>
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
            </li>
          </ul>
        </div>
        <div class="social-media-box">
          <ul>
            <li>
              <fontawesome-icon
                class="projects-icon"
                :icon="['fab', 'instagram']"
              />
            </li>
            <li>
              <fontawesome-icon
                class="projects-icon"
                :icon="['fab', 'facebook-f']"
              />
            </li>
            <li>
              <fontawesome-icon
                class="projects-icon"
                :icon="['fab', 'github']"
              />
            </li>
            <li>
              <fontawesome-icon
                class="projects-icon"
                :icon="['fab', 'linkedin']"
              />
            </li>
            <li>
              <fontawesome-icon
                class="projects-icon"
                :icon="['fab', 'twitter']"
              />
            </li>
            <li>
              <fontawesome-icon class="projects-icon" :icon="['fab', 'xing']" />
            </li>
          </ul>
        </div>
      </div>
      <div class="map-box col-md-5">
        <iframe
<<<<<<< HEAD
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d38843.48101713569!2d13.459642512002427!3d52.52045023234101!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47a84e9772a20769%3A0x1c212049953de6f0!2s10365%20Berlin!5e0!3m2!1sen!2sde!4v1635502754837!5m2!1sen!2sde"
=======
          src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d77681.80044292015!2d13.348991292695041!3d52.52336906445637!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47a84e373f035901%3A0x42120465b5e3b70!2sBerlin%2C%20Germany!5e0!3m2!1sen!2s!4v1631263011067!5m2!1sen!2s"
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
          width="400"
          height="350"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "contactView",
};
</script>
<style lang="scss">
<<<<<<< HEAD
$yellowCol: rgb(230, 173, 67);
$permanentFont: "Permanent Marker", cursive;
$kashenFont: "Kaushan Script", cursive;
$meriendaFont: "Merienda", cursive;
$luckiestFont: "Luckiest Guy", cursive;
.contact-view {
  .title {

=======
$yellowCol:rgb(230, 173, 67);


.contact-view {
  .title {
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
    h1 {
      left: 35%;
    }
    h3 {
      left: 35%;
    }
  }
  .contact-container {
    width: 100%;
    height: 480px;
    .contact-box {
      .informarion-box {
        ul {
          text-align: left;
          margin-top: 150px;
          letter-spacing: 2px;
          color: $yellowCol;
          list-style-type: none;
          font-size: 15.2px;
          .details-title {
            font-weight: bolder;
            color: rgb(233, 233, 233);
            font-size: 17.5px;
<<<<<<< HEAD
            font-family: $kashenFont;
=======
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
          }
        }
      }
      .social-media-box {
        margin-top: 70px;
        ul {
          list-style-type: none;
          li {
            float: left;
            width: 8%;
            height: 45px;
            background: rgba(255, 0, 0, 0.014);
            margin-right: 4%;
            font-size: 28px;
            border-radius: 50%;
            cursor: pointer;
            color: $yellowCol;
            transition: all 0.4s ease-in-out;
            .projects-icon {
              padding-left: 2%;
            }
            &:hover {
              background: $yellowCol;
              color: black;
              border: 2px solid rgb(214, 152, 37);
            }
          }
        }
      }
    }
    .map-box {
      iframe {
        margin-top: 80px;
<<<<<<< HEAD
        width: 100%;
=======
width: 100%;
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
        border-radius: 2%;
        box-shadow: 0px 1px 4px $yellowCol;
      }
    }
  }
}
@media only screen and (max-width: 570px) {
<<<<<<< HEAD
  .contact-view .title {
    h1 {
      left: 8%;
      top: -35px;
      font-size: 55px;
    }
    h3 {
      left: 7%;
      font-size: 29px;
      letter-spacing: 7px;
    }
  }
  .contact-view .contact-container .contact-box .informarion-box ul {
    margin-top: 80px;
  }
=======
 
   .contact-view .title{
      h1{
      left: 8%;
       top: -35px;
      font-size:55px;
      }
      h3 {
        left: 7%;
       font-size:29px;
       letter-spacing: 7px;
      }
    
   }
   .contact-view .contact-container .contact-box .informarion-box ul{
     margin-top: 80px;
   }
>>>>>>> 429a8294a2d71270560967dfd269f9fb3c2fc305
}
</style>
