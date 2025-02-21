<template>
  <div :class="c1">
    <div :class="c2">
      <div class="main" id="main">
        <div class="banner"></div>
        <div class="vNN"></div>
        <video class="vN" autoplay muted loop>
          <source src="../assets/Main/wheelMovie.mp4" type="video/mp4">
        </video>
        <div class="appCenter">
          <div class="ac1"><img src='../assets/Main/qrcode.jpg' alt="qrcode"></div>
          <div class="ac2">
            <img src="../assets/Main/download1.png" alt="download" class="ac2a">
            <img src="../assets/Main/download2.png" alt="download" class="ac2a">
            <img src="../assets/Main/download3.png" alt="download" class="ac2b">
            <img src="../assets/Main/download4.png" alt="download" class="ac2a">
            <img src="../assets/Main/download5.png" alt="download" class="ac2a">
            <img src="../assets/Main/download6.png" alt="download" class="ac2b">
          </div>
        </div>
        <div class="center">
          <img src="../assets/Main/share1.png" alt="no">
          <img src="../assets/Main/share2.png" alt="no">
          <img src="../assets/Main/share3.png" alt="no">
          <img src="../assets/Main/share4.png" alt="no">
        </div>
        <div class="activity">
          <p>活动</p>
        </div>
        <div class="option">
          <div class="language">
            <div class="languageIcon">
              <img src="../assets/Main/language.png" alt="no">
            </div>
            <p>简体中文</p>
            <div class="languageOption" @click='ccc'></div>
          </div>
          <div class="sound">
            <div></div><div></div><div></div>
          </div>
          <div class="user">
            <img src="../assets/Main/user.png" alt="no">
          </div>
        </div>
        <div class="tips">
          <img src="../assets/Main/scroll.png" alt="no">
        </div>
      <News />
      <Esonators />
      <Lore />
      <Regions />
      <End />

    </div>
  </div>
  <div :class="c3">
    <div :class="c3a">
      <a v-for="c2fv in c2fName" :href="c2fv.href " @click="link" :id="c2fv.num">
        <div></div>
        {{ c2fv.name }}</a>
    </div>
  </div>
    <div :class=c3i>
      <img src='../assets/Main/logo-small.png' alt="no">
    </div>
  </div>
</template>

<script>
import News from '@/components/News.vue';
import Esonators from '@/components/Esonators.vue';
import Lore from '@/components/Lore.vue';
import Regions from '@/components/Regions.vue';
import End from '@/components/End.vue';

export default {
  components: {Esonators, End,Regions, Lore, News},
  data(){
    return {
      mainDiv:  [{'name':'main',href:'#main'},{'name':'news',href:'#news'},{'name':'esonators',href:'#esonators'},{'name':'lore',href:'#lore'},{'name':'regions'},{'name':'characters',href:'#characters'},{'name':'gallery',href:'#gallery'},{'name':'community',href:'#community'},{'name':'end',href:'#end'}],
      c2fName:  [{'name':'首页',href:'#main','num':'1'},{'name':'资讯',href:'#news','num':'2'},{'name':'共鸣者',href:'#esonators','num':'3'},{'name':'情报',href:'#lore','num':'4'},{'name':'世界',href:'#regions','num':'5'},{'name':'储值中心',href:'https://github.com/BLACKSHARKPLAYBT','num':'6'}],
      //一些名称
      c1:'content',c2:'viewer',c3:'c2f',c3a:'c2fCenter',
      videoName:'vN',c3i:'logo',
    }
  },
  mounted() {
    let aaa = document.querySelectorAll('.c2f .c2fCenter a div');
    let a = document.querySelectorAll('.c2f .c2fCenter a');
    aaa[0].style.opacity='1';
    a[0].style.color='#c9ac67';
  },
  methods:{
  link(){
    let test=event.target.id - 1;
    let aaa = document.querySelectorAll('.c2f .c2fCenter a div');
    let a = document.querySelectorAll('.c2f .c2fCenter a');
    for(let i=0;i<aaa.length;i++){
      aaa[i].style.opacity="0";
      a[i].style.color='#ffffff';
      }
  aaa[test].style.opacity="1";
  a[test].style.color='#c9ac67';},
  ccc(){
      let ccc =document.querySelector('#main > div.option > div.language > div.languageOption');
      console.log(ccc);
    }
  }
}
</script>
<style scoped>
/* c2f */
.c2f  {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 20vh;
  background-color: rgba(0,0,0,0);
  z-index: 999;
  display: flex;
  justify-content: center;
}

.c2f .c2fCenter {
  position: fixed;
  display: flex;
  justify-content: center;
}

.c2f .c2fCenter a {
  margin-top: 10px;
  margin-left: 40px;
  padding: 18px;
  height: 1px;
  color: snow;
  font-size: 12.5px;
  font-family: mc-gamefont;
  font-weight: 700;
  transition-duration: 500ms;
  transition-delay: 0.3s;
  transition: opacity 2s ease;
}

.c2f .c2fCenter a:link {
  text-decoration: none;

}

.c2f .c2fCenter a:nth-child(3n+1) div {
  width: 2rem;
  height: 1rem;
  background-image: url("@/assets/Main/hoverTop.png");
  transform:translateX(-0.2rem);
  opacity: 0;
}

.c2f .c2fCenter a:nth-child(3n+1) div::before {
  content: "";
  background: url("@/assets/Main/hoverLeft.png") no-repeat;
  background-size: 100% 100%;
  width: 9.45rem;
  height: 2.4rem;
  position: absolute;
  top: 0;
  left: -9.47rem;
  pointer-events: none;
}

.c2f .c2fCenter a:nth-child(3n+1) div::after {
  content: "";
  background: url("@/assets/Main/hoverRight.png") no-repeat;
  background-size: 100% 100%;
  width: 9.5rem;
  height: 2.4rem;
  position: absolute;
  top: 0;
  right: -9.5rem;
  pointer-events: none;
}

.c2f .c2fCenter a:nth-child(3n+2) div{
  width: 2rem;
  height: 1rem;
  background-image: url("@/assets/Main/hoverTop.png");
  transform: translateY(-0.2rem) translateX(-0.2rem);
  opacity: 0;
}

.c2f .c2fCenter a:nth-child(3n+2) div::before {
  content: "";
  background: url("@/assets/Main/hoverLeft.png") no-repeat;
  background-size: 100% 100%;
  width: 9.5rem;
  height: 2.4rem;
  position: absolute;
  top: 0;
  left: -9.5rem;
  pointer-events: none;
}

.c2f .c2fCenter a:nth-child(3n+2) div::after {
  content: "";
  background: url("@/assets/Main/hoverRight.png") no-repeat;
  background-size: 100% 100%;
  width: 9.5rem;
  height: 2.4rem;
  position: absolute;
  top: 0;
  right: -9.5rem;
  pointer-events: none;
}

.c2f .c2fCenter a:nth-child(3) div{
  width: 3rem;
  height: 1rem;
  background-image: url("@/assets/Main/hoverTop.png");
  transform: translateY(-0.3rem) translateX(-0.2rem);
  opacity: 0;
}

.c2f .c2fCenter a:nth-child(3) div::before {
  content: "";
  background: url("@/assets/Main/hoverLeft.png") no-repeat;
  background-size: 100% 100%;
  width: 9.5rem;
  height: 2.4rem;
  position: absolute;
  top: 0;
  left: -9.5rem;
  pointer-events: none;
}

.c2f .c2fCenter a:nth-child(3) div::after {
  content: "";
  background: url("@/assets/Main/hoverRight.png") no-repeat;
  background-size: 100% 100%;
  width: 9.5rem;
  height: 2.4rem;
  position: absolute;
  right: -9.47rem;
  pointer-events: none;

}

.c2f .c2fCenter a:nth-child(6) div{
  width: 3rem;
  height: 1rem;
  background-image: url("@/assets/Main/hoverTop.png");
  transform: translateY(-0.3rem) translateX(-0.2rem);
  opacity: 0;
}

.c2f .c2fCenter a:nth-child(6) div::before {
  content: "";
  background: url("@/assets/Main/hoverLeft.png") no-repeat;
  background-size: 100% 100%;
  width: 9.5rem;
  height: 2.4rem;
  position: absolute;
  top: 0;
  left: -9.52rem;
  pointer-events: none;
}

.c2f .c2fCenter a:nth-child(6) div::after {
  content: "";
  background: url("@/assets/Main/hoverRight.png") no-repeat;
  background-size: 100% 100%;
  width: 9.5rem;
  height: 2.4rem;
  position: absolute;
  right: -9.47rem;
  pointer-events: none;

}

.logo {
  position: fixed;
  left:20px;
  top:20px;
  width: 9.5rem;
  height: 3.8rem;
  z-index: 999;
}
.logo img {
  width: 100%;
  height: 100%;
}

.banner {
  position: fixed;
  background: linear-gradient(rgba(0,0,0,1),rgba(0,0,0,0.01));
  width: 100%;
  height: 16.5vh;
  z-index: 1000;
  left: 0;
  top: 0;
}



/* display */
.content {
  top:0;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: flex-start;
  overflow: hidden;
  position: fixed;
}

.viewer{
  position: relative;
  flex-shrink: 0;
  width: 100%;
  display: flex;
  flex-direction: column;
  transition: 500ms ease;
  transition-delay: 0.3s;
  transition-duration: 500ms;
}

.viewer > div{
  width: 100%;
  height: 100vh;
  background-color: yellow;
}

/* main */
.main {
  background-image: url(../assets/Main/wheelBeforeMovie.jpg);
  background-size: cover;
  z-index: 997;
  transition: 500ms ease;
  transition-delay: 0.3s;
  transition-duration: 500ms;
}


.vN {
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 998;
}

.main .vNN {
  height: 3rem;
  width: 3rem;
  position: absolute;
  background-image: url("@/assets/Main/play.png");
  background-size: cover;
  top:calc(50% - 1.5rem);
  left: calc(50vw - 1.5rem);
  z-index: 1000;
  transition: 400ms;
}

.main .vNN:hover {
  opacity: 0.4;
}

.main .appCenter {
  display: flex;
  justify-content: center;
  align-items: center;
  left: calc(100% - 73vw);
  bottom: calc(20vh - 65px);
  z-index:999;
  width: 50vw;
  height: 135px;
  position: absolute;
}

.main .appCenter .ac1  {
  outline: 1px solid #a6a6a6;
  border: 7px solid rgba(0,0,0,0.2);
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.main .appCenter .ac1 img {
  width: 5.9rem;
  height: 5.9rem;
}

.main .appCenter .ac2  {
  display: flex;
  flex-wrap: wrap;
  width: calc(50vw - 8rem);
  margin-left: 10px;
  row-gap: 20px;
  column-gap: 10px;
}

.main .appCenter .ac2 .ac2a {
  height: 2.8rem;
  margin-left: 5px;
}

.main .appCenter .ac2 .ac2b{
  height: 2.8rem;
}

.center {
  width: 130px;
  height: 30px;
  position: absolute;
  bottom: 30px;
  left: 50px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
}

.center img {
  width: 1.35rem;
  height: 1.35rem;
}

.main .activity {
  position: absolute;
  right:0;
  bottom: 25vh;
  width: 90px;
  height: 28px;
  border-width:1px 0 3px 1px;
  border-style: solid;
  border-color: #c9ac67;
  background-color: rgba(0,0,0,0.5);
}
.main .activity p{
  font-size: 0.6rem;
  color: white;
  font-family: mc-gamefont;
  margin-top: 5px;
  margin-left: 6px;
}

/*   右上角选项   */
.option {
  width: 200px;
  height: 50px;
  position: fixed;
  right: 45px;
  top: 20px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  z-index: 1000;
}
.option .language {
  height: 28px;
  width: 120px;
  border: 1px solid white;
  display: inline-flex;
  gap: 0.5rem;
  justify-content: center;
  align-items: center;
}

.option .language .languageIcon {
  width: 1.5rem;
  height: 1.5rem;
}

.option .language .languageIcon img {
  width: 100%;
  height: 100%;
}

.option .language p {
  font-family: mc-gamefont;
  font-size: 11px;
  color: white;
}

.option .language .languageOption {
  width: 0.5rem;
  height: 0.35rem;
  background-color: white;
  clip-path: polygon(0 0,100% 0%,50% 100%);
}

.option .sound {
  width: 1.5rem;
  height: 1.5rem;
  border: 1px solid white;
  border-radius: 50%;
  display: inline-flex;
}

.option .sound div:nth-child(1) {
  width: 0.16rem;
  height: 0.5rem;
  background-color: #c9ac67;
  border-radius: 25%;
  transform: translateX(0.3rem) translateY(0.5rem);
}

.option .sound div:nth-child(2) {
  width: 0.16rem;
  height: 0.8rem;
  background-color: #c9ac67;
  transform: translateX(0.5rem) translateY(0.3rem);
  border-radius: 25%;
}

.option .sound div:nth-child(3) {
  width: 0.16rem;
  height: 0.5rem;
  background-color: #c9ac67;
  transform: translateX(0.7rem) translateY(0.5rem);
  border-radius: 25%;
}

.option .user {
  width: 2rem;
  height: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.option .user img {
  width: 1.4rem;
  height: 1.4rem;
}

.main .tips {
  width: 3rem;
  height: 3rem;
  position: absolute;
  bottom: 10px;
  right: 40px;
}

.main .tips img {
  width: 100%;
  height: 100%;
}

.main .tips {
  animation: tipMove 5s linear infinite;
  transition: 500ms;
}
@keyframes tipMove {
  0% {
    transform: translateY(0);
  }
  25% {
    transform: translateY(10px);
  }
 50% {
    transform: translateY(0);
  }
  75% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0);
  }
}
</style>
