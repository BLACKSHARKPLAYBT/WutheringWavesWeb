<script setup>
const info1 = "黎那汐塔"
const info2 = "RINASCITA"
const info3 = "由群島上的數個高度獨立的城邦組成的國家，並不存在傳統意義上的政治中心。傳說中，黎那汐塔人的先祖為了從悲鳴中倖存，從另一片土地渡海遷徙而來。\n" +
    " 黎那汐塔人憑藉著名為「公共聲骸」的特殊聲骸技術，將聲骸廣泛運用在了生活中的各個方面。「聲骸之國」的別稱也正是由此而來。"
</script>

<template>
  <div class="regions" id="regions">
    <div class="mixed"><img src="@/assets/Regions/bg.png" alt=""></div>
      <div class="part1">
        <p>世界展示</p>
      </div>
      <div class="part2">
        <div class="item"><img src="@/assets/Regions/rg1.jpg"></div>
        <div class="item"><img src="@/assets/Regions/rg2.jpg"></div>
      </div>
      <div class="part3">
        <div><p>{{info1}}</p><p>{{info2}}</p></div>
        <p>{{info3}}</p>
      </div>
  </div>
</template>

<style scoped>
img {
  width: 100%;
  height: 100%;
}

.regions{
  width: 100%;
  height: 100vh;
  background-image: url("@/assets/Regions/bg2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  transition: 500ms ease;
  transition-delay: 0.5s;
  transition-duration: 500ms;
  display: flex;
  flex-direction: column;
  z-index: 2;
}

.regions .mixed{
  width: 100%;
  height: 100%;
  z-index: 1;
  position: absolute;
}

/*  主界面  */
.part1{
  width: 20rem;
  height: 10rem;
  position: relative;
  z-index: 3;
  white-space: nowrap;
  top: 6.5rem;
  left: 3.5rem;
}

.part1 p{
  color: #c9ac67;
  font-size: 20px;
}

.part2 {
  width: 100%;
  height: 60vh;
  position: relative;
  z-index: 2;
  top: 0;
  left: 0;
  overflow: hidden;
  display: inline-flex;
  gap: 20px;
  border: solid #c9ac67;
  border-right: 2px;
  justify-content: space-around;
}

.part2 .item:nth-child(1){
  width: 80%;
  height: 95%;
}

.part2 .item:nth-child(2){
  width: 20%;
  height: 95%;
  opacity: 0.3;
}

.part3 {
  width: 100%;
  height: 20vh;
  position: relative;
  z-index: 2;
  top: 0;
  left: 0;
  display: flex;
  justify-content: left;
  align-items: center;
}

.part3 div{
  width: 20%;
  height:100%;
  position: relative;
  top: 50px;
  left: 0;
}

.part3 div p{
  color:  #c9ac67;
  font-family: mc-gamefont, sans-serif;
  font-size: 35px;
  text-align: center;
}

.part3 div p:nth-child(2){
  font-size: 12px;
}

.part3 p{
  color:  #c9ac67;
  font-family: mc-gamefont, sans-serif;
  font-size: 13px;
  white-space: pre-wrap;
}
</style>