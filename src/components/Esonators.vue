<script setup>
function Title() {
}
function Icon(){
}
function Selector(){
}

function clicked(){
  console.log("clicked");
}

const name1 = "UNKOWN";
const name2 = "未知";

</script>

<template>
  <div class="esonaters" id="esonators">
    <div class="shower">
      <div class="bar">
        <div class="icon" @click="clicked">
          <img src="@/assets/Esonaters/icon1.png" alt="">
          <img src="@/assets/Esonaters/icon1h.png" alt="">
        </div>
        <div class="icon" @click="clicked">
          <img src="../assets/Esonaters/icon2.png" alt="">
          <img src="../assets/Esonaters/icon2h.png" alt="">
        </div>
        <div class="icon" @click="clicked">
          <img src="@/assets/Esonaters/icon3.png" alt="">
          <img src="@/assets/Esonaters/icon3h.png" alt="">
        </div>
        <div class="icon" @click="clicked">
          <img src="@/assets/Esonaters/icon4.png" alt="">
          <img src="@/assets/Esonaters/icon4h.png" alt="">
        </div>
        <div class="icon" @click="clicked">
          <img src="../assets/Esonaters/icon5.png" alt="">
          <img src="../assets/Esonaters/icon5h.png" alt="">
        </div>
      </div>
      <div class="selector">
        <div class="section1">
          <div class="logo-shower">
            <div class="logo">
              <img src="@/assets/Esonaters/logo1.png" alt="">
            </div>
            <div class="line"></div>
            <div class="line-box">
              <p>{{name1}}</p>
              <p>{{name2}}</p>
              <img src="@/assets/Esonaters/text-after.png" alt="">
            </div>
            <div class="line"></div>
          </div>
        </div>
        <div class="section2">
          <div class="viewbox">
            <img src="@/assets/Esonaters/C%20rover2.png" alt="">
          </div>
          <div class="viewbox">
            <img src="@/assets/Esonaters/C%20rover1.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

img {
  width: 100%;
  height: 100%;
}

#esonators {
  width: 100%;
  height: 100vh;
  background-image: url("@/assets/Esonaters/bg.jpg");
  display: flex;
  justify-content: center;
  align-items: center;
}
#esonators .shower {
  width: 100vw;
  height: 80%;
  background-color: rgba(0,0, 0, 0.1);
  top: 20px;
  position: relative;
}


/*    地区图标    */
.shower .bar {
  top: 20px;
  width: 10%;
  height: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 3;
  gap: 30px;
}

.shower .bar .icon {
  width: 4rem;
  height: 4rem;
  background-color: rgba(0, 0, 0, 0);
  z-index: 4;
  margin-top: 15px;
}

.shower .bar .icon img{
  width: 100%;
  height: 100%;
}

.shower .bar .icon img:nth-child(2) {
  opacity: 0;
}

/*    角色展示卡   */
.shower .selector {
  width: 85%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.1);
  position: absolute;
  top: 0;
  left: 15%;
  z-index: 2;
  display: inline-flex;
}

/* 左部分  */
.shower .section1{
  width: 40%;
  height: 100%;
}

.shower .section1 .logo-shower {
  width: 100%;
  height: 120%;
}

.shower .section1 .logo-shower .logo{
  width: 18rem;
  height: 15rem;
  margin-left: calc(50% - 10rem);
}

.shower .section1 .logo-shower .line {
  width: 95%;
  height: 0.5px;
  background-color: #e1e1e1;
}

.shower .section1 .logo-shower .line:nth-child(2) {
  position: relative;
  bottom: 0;
}

.shower .section1 .logo-shower .line-box{
  width: 100%;
  height: 40%;
  background-color: rgba(0, 0, 0, 0);
  margin: 0.5rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  top: 10px;
}

.selector > .section1 > div > .line-box > p{
  width: 60px;
  height: 40px;
  font-size: 50px;
  color: #e1e1e1;
  position: relative;
  top: 30px;
  left: -200px;
  white-space: nowrap;
  font-family: mc-gamefont, sans-serif;
}
.selector > .section1 > div > .line-box > p:nth-child(2){
  margin-top: 20px;
}

.selector > .section1 > div > .line-box > img{
  width: 90%;
  height: 30%;
  position: relative;
  bottom: -100px;
  left: 0;
}
  /*   右部分  */
.selector .section2{
  top: 10px;
  left: 0;
  width: 60%;
  height: 90%;
  position: relative;
  overflow: hidden;
  display: inline-flex;
  gap: 5px;
}

.selector .section2 .viewbox {
  width: 13rem;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.3);
  overflow: hidden;
  border: 1px solid rgba(201, 172, 103, 0.44);
  transition-duration: 100ms;
  transition-delay: 100ms;
  transition-timing-function: ease-in-out;
  transition: 0.5s;
}

.selector .section2 .viewbox img{
  width: 15rem;
  height: 100%;
  background-repeat: no-repeat;
  background-size: cover;
  opacity: 0.6;
  transition-duration: 100ms;
  transition-delay: 100ms;
  transition-timing-function: ease-in-out;
  transition: 0.5s;
}

/*  悬停效果  */
.selector .section2 .viewbox:hover{
  width:18rem;
}
.selector .section2 .viewbox:hover img{
  transform: translateX(40px);
  width:15rem;
}
</style>