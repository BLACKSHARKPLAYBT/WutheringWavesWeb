<script setup>
const name1 = "Waveworn Phenomenon";
const name2 = "海蚀現象";
const description = "悲鳴之下，毀滅的浪潮對索拉世界產生了侵蝕作用。\n" +
    "「無音區」、「殘象潮」、「黑石」……種種在此顯露出的侵蝕異象表現統稱為「海蝕現象」。"
</script>

<template>
  <div class="lore" id="lore">
    <div class="container">
      <div class="left">
        <div class="ic">
          <img src="@/assets/Lore/icon.png" alt="" />
        </div>
        <div class="text">
          <p>{{name1}}</p>
          <p>{{name2}}</p>
          <p>{{description}}</p>
        </div>
      </div>
   <div class="right">
     <div class="left">
       <img src="@/assets/Lore/left-arrow.png" alt="" />
     </div>

     <div class="router">
       <div class="item"><img src="@/assets/Lore/bbgg1.jpg" alt=""></div>
       <div class="item"><img src="@/assets/Lore/bbgg2.jpg" alt=""></div>
       <div class="item"><img src="@/assets/Lore/bbgg3.jpg" alt=""></div>
     </div>

     <div class="right">
       <img src="@/assets/Lore/right-arrow.png" alt="" />
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

.lore {
  width: 100%;
  height: 100vh;
  background-image: url("@/assets/Lore/bg.jpg");
  transition: 500ms ease;
  transition-delay: 0.3s;
  transition-duration: 500ms;
  display: flex;
  justify-content: center;
  align-items: center;}

.lore .container {
  width:90%;
  height: 85%;
  top: 5%;
  position: relative;
  display: inline-flex;
}

/*   左部分   */

.lore .container .left {
  width: 40%;
  height: 100%;
  position: relative;
}

.ic{
  width: 22rem;
  height: 22rem;
  top: 0;
  left: calc(50% - 11rem);
  position: relative;
}

.lore .container .left .text{
  width: 100%;
  height: 40%;
  position: relative;
  bottom: 0;
  left: 0;
  border: solid rgba(255, 247, 237, 0.16);
  border-left: 0.1rem;
  border-right: 0.1rem;
  display: flex;
  flex-direction: column;
}

.lore .container .left .text p{
  color: gray;
  font-size: 3rem;
  font-weight: bold;
  position: relative;
  white-space: pre-wrap;
  left: 20px;
  line-height: 3rem;
  font-family: mc-gamefont, sans-serif;
}

.lore .container .left .text p:nth-child(2){
  top: 10px;
  line-height: 3.5rem;
}

.lore .container .left .text p:nth-child(3){
  top: 40px;
  font-size: 0.6rem;
  line-height: 0.6rem;
}
/*    右部分    */

.lore .container .right {
  width: 60%;
  height: 100%;
  position: relative;
  display: inline-flex;
}

.lore .container .right .left {
  width: 3rem;
  height: 3rem;
  position: relative;
  left: 0;
  top: 50%;
}

.lore .container .right .right {
  width: 3rem;
  height: 3rem;
  position: relative;
  right: 0;
  top: 50%;
}

/* 轮播图 */
.lore .container .right .router {
  width: 100%;
  height: 100%;
  position: relative;
  display: inline-flex;
  justify-content: flex-start;
  overflow: hidden;
  gap: 10px;
}

.lore .container .right .router .item{
  border: 2px solid #b5986a;
}

.lore .container .right .router .item:nth-child(1) {
  width: 20rem;
  height: 100%;
  opacity: 1;
}

.lore .container .right .router .item:nth-child(2) {
  width: 15rem;
  height: 100%;
  opacity: 0.3;
}

.lore .container .right .router .item:nth-child(3) {
  width: 15rem;
  height: 100%;
  opacity: 0.3;
}
</style>