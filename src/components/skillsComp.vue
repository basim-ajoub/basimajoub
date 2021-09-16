<template>
    <div class="skills-comp">
<ul>
            <li class="row">
              <span class="details-title col-md-4">Programming Languages:</span
              ><span class="col-md-8">HTML - CSS - Java Scripts - Python.</span>
            </li>
                        <li class="row">
              <span class="details-title col-md-4">Programming Library:</span
              ><span class="col-md-8">JQuery - SASS .</span>
            </li>
            <li class="row">
              <span class="details-title col-md-4">FrameWork:</span
              ><span class="col-md-8">Vue.Js .</span>
            </li>
            <li class="row">
              <span class="details-title col-md-4">Computer Skills:</span
              ><span class="col-md-8">PhotoShop - Git - Visual Studio Code .</span>
            </li>
            <li class="row">
              <span class="details-title col-md-4">Speaking Languages :</span
              ><span class="col-md-8">German (B1) - English (IELTS - C1) - Arabic (Native) .</span>
            </li>
              <li class="row">
              <span class="details-title col-md-4">Completed Projects :</span
              ><span class="col-md-8">07 .</span>
            </li>
          </ul>
    </div>
</template>
<script>
export default {
    name:"SkillsComp",
}
</script>
<style lang="scss">
$permanentFont: "Permanent Marker", cursive;
$kashenFont: "Kaushan Script", cursive;
$meriendaFont: "Merienda", cursive;
$luckiestFont: "Luckiest Guy", cursive;
$yellowCol:rgb(230, 173, 67);

.skills-comp{
    position: absolute;
    width: 70%;
    height: 475px;
   // background: rgba(255, 0, 0, 0.274);
    z-index: 31;
       ul {
          text-align: left;
          margin-top: 110px;
          letter-spacing: 1px;
          color: $yellowCol;
          list-style-type: none;
          font-size: 15.2px;
          font-family: $meriendaFont;
          li{
              margin-bottom: 20px;
          }
          .details-title {
              letter-spacing: 2px;
            font-weight: bolder;
            color: rgb(233, 233, 233);
            font-size: 16px;
            font-family: $kashenFont;
          }
        }
}
</style>