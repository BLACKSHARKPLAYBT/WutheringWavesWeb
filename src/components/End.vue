<script setup>
const below = "本遊戲為免費使用，遊戲內另提供購買虛擬貨幣、物品等付費服務。\n" +
    "請注意遊戲時間，避免沉迷。\n" +
    "本遊戲部分情節涉及性、暴力。\n" +
    "隱私權政策  使用者協議\n" +
    "客服信箱為 wutheringwaves@nijigengames.com\n" +
    "©HK KURO GAMES LIMITED. All Rights Reserved.\n" +
    "Epic, Epic Games, Epic Games Store, the Epic Games Store logo, and Epic Online Services are trademarks and/or registered trademarks of Epic Games. All other trademarks are the property of their respective owners."
</script>

<template>
  <div class="end" id="end">
    <div class="bg">
      <video src="@/assets/End1/end.mp4" autoplay muted></video>
    </div>
    <div class="share">
      <a><img src="@/assets/End1/share1.png" alt=""></a>
      <a><img src="@/assets/End1/share2.png" alt=""></a>
      <a><img src="@/assets/End1/share3.png" alt=""></a>
      <a><img src="@/assets/End1/share4.png" alt=""></a>
    </div>
  </div>
  <div class="end2" id="end2">
    <div class="part1">
      <img src="@/assets/End2/kurogame.png" alt="">
      <img src="@/assets/End2/nji.png" alt="">
      <img src="@/assets/End2/15.png" alt="">
    </div>
    <div class="part2"><p>{{below}}</p></div>
  </div>
</template>

<style scoped>

img {
width: 100%;
  height: 100%;
}


.end{
  width: 100%;
  height: 100vh;
  background-image: url("../assets/End1/end1.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  transition: 500ms ease;
  transition-delay: 0.3s;
  transition-duration: 500ms;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  flex-direction: column;
}

.end .bg {
  position: relative;
  top: -100px;
  left: -350px;
  width: 50vw;
  height: 50vh;
}

.end .bg video{
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 1;
  mix-blend-mode: screen;
}

.end .share {
  width: 200px;
  height: 40px;
  position: relative;
  bottom: -100px;
  left: -600px;
  z-index: 3;
  display: inline-flex;
  justify-content: space-between;
}

.end .share a {
  width: 30px;
  height: 30px;
}


/*  页尾  */

.end2 {
  width: 100%;
  height: 20vh;
  background-color: snow;
  display: inline-flex;
  justify-content: center;
  align-items: center;
}

.end2 .part1 {
  width: 40%;
  height: 100%;
  display: inline-flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 40px;
  position: relative;
  left: 100px;
}


.end2 .part1 img:nth-child(1){
  width:180px;
  height: 60px;
}
.end2 .part1 img:nth-child(2){
  width: 60px;
  height: 60px;
}
.end2 .part1 img:nth-child(3){
  width: 60px;
  height: 60px;
}

.end2 .part2{
  left: 80px;
  top:10px;
  position: relative;
}

.end2 .part2 p {
  width:60%;
  height: 100%;
  position: relative;
  font-size: 12px;
  white-space: pre-wrap;
  color: #a6a6a6;
  line-height: 16px;
}
</style>