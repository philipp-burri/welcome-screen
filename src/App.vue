<script setup>
/* import { ref } from 'vue';

const content = ref ([
{
  date: 'currentDate'
}
]
 */
 let date = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));
let options = { /* weekday: 'long',  */ year: 'numeric', month: 'numeric', day: 'numeric' };
</script>

<template>



<main>
    <div class="wrapper">
    <div class="title">Welcome to Opportunity</div>
    <div class="date">{{ new Date().toLocaleString("de-ch", options) }}</div>
    <div class="info">
  <div class="info-card">
    <ul>
      
        <li><div class="info-time"><b>14:00 Uhr</b></div></li>
       <li><div class="info-title"><b>Basisbeschäftigung Besuch</b></div></li>
        <li><div class="info-desc">Interessierte für den zweiten Kurs werden uns besuchen</div></li>
      
    </ul>
  </div>
  <div class="info-card">
    <ul>
      
      <li><div class="info-time"><b>14:00 Uhr</b></div></li>
     <li><div class="info-title"><b>Basisbeschäftigung Besuch</b></div></li>
      <li><div class="info-desc">Interessierte für den zweiten Kurs werden uns besuchen</div></li>
    
  </ul>
  </div>
  <div class="info-card">
    <ul>
      
      <li><div class="info-time"><b>14:00 Uhr</b></div></li>
     <li><div class="info-title"><b>Basisbeschäftigung Besuch</b></div></li>
      <li><div class="info-desc">Interessierte für den zweiten Kurs werden uns besuchen</div></li>
  </ul>
  </div>
</div>
    </div>
<div class="footer">
  <div class="icon-container">
    <img class="icon1" src="/STZH_SEB_Logo.png" alt="">
    <img class= "icon2" src="/Opportunity.png" alt="">
    <img class="icon3" src="/SAG_Logo_De.png" alt="">
  </div>
</div>

   

</main> 




</template>

<style scoped>

main{
  background-color: #E8EFF4;
  width: 1080px;
  height: 1920px;
  font-family: "Inter", sans-serif;
  min-height: 100vh;
}

  .wrapper {
  margin-left: 60px;
  flex: 1;
}

ul{
  list-style: none;
}
.title{
  padding-top: 70px;
  font-size: 62px;
  font-weight: 900;
  color: #323D4A;
}

.date{
  margin-top: 21px;
  font-size: 62px;
  font-weight: 500;
  color: #9AA7B1;
}
.info{
  display: flex;
  flex-direction: column;
  gap: 40px;
  margin-top: 36px;
}

.info-card{
  background-color: #0F05A0 ;
  padding-top: 35px;
  padding-bottom: 40px;
  margin-left: 0;
  gap: 10px;
  width: 960px;
  
}
.info-time{
  color: #EB5E00;
  font-size: 28px;
  font-weight: 900;
}
.info-title{
  color: #FFBFAB;
  font-weight: 900;
  font-size: 28px;
}
.info-desc{
  color: #FFBFAB;
  font-size: 28px;
}

.footer{
  display: flex;
  background-color: white;
  height: 130px;
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  align-items: center;
  
}
.icon-container{
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
  margin-right: 40px;
  margin-left: 40px;
}

.icon1{
  width: 230px;
  height: 44px;
  align-items: center;
}

.icon2{
  width: 296px;
  height: 55px;
}

.icon3{
width: 273px;
height: 52px;
}

</style>

