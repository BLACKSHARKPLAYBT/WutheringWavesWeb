<script setup>

</script>

<template>
  <div class="new" id="news">
    <div class="news">
      <p>NEWS</p>
      <div class="line"></div>
      <div class="nav">
        <a>最新<div></div></a>
        <a>活动<div></div></a>
        <a>新闻<div></div></a>
        <a>公告<div></div></a>
      </div>
      <div class="line"></div>
    </div>
    <div class="newsContainer">
      <div class="article">
        <p>公告</p>
        <div class="message">声骸材料限时双倍活动</div>
      <div class="lll"></div>
        <div class="ll"></div>
      </div>
      <div class="article">
        <p>公告</p>
        <div class="message">极限拉古那限时多人竞速跑酷活动</div>
        <div class="lll"></div>
        <div class="ll"></div>
      </div>
      <div class="article">
        <p>公告</p>
        <div class="message">鸣潮×Mycard飞鸟轻鸣浪清欢唱</div>
        <div class="lll"></div>
        <div class="ll"></div>
      </div>
      <div class="article">
        <p>新闻</p>
        <div class="message">《鸣潮）《飞鸟轻，浪涛饮唱》创作徽集活动</div>
        <div class="lll"></div>
        <div class="ll"></div>
      </div>
      <div class="article">
        <p>公告</p>
        <div class="message">飞鸟繁唱，浪漂款唱，2.1版本内容说明</div>
        <div class="lll"></div>
        <div class="ll"></div>
      </div>
      <div class="article">
        <p>公告</p>
        <div class="message">《鸣潮》2.0版本「致臧默以歌」创作徽集活动覆奖名军</div>
        <div class="lll"></div>
        <div class="ll"></div>
      </div>

    </div>
    <div class="router">
      <img src="@/assets/News/router-img1.jpg" alt="">
      <img src="" alt="">
    </div>
    <div class="BG"></div>
    <div class="footerBg">
      <video src="@/assets/News/bg-wave.mp4" type="mp4" autoplay muted loop></video>
    </div>
  </div>
</template>

<style scoped>
  .new {
    top: 20px;
    width: 100%;
    height: 100vh;
    background-color: yellow;
    transition: 500ms ease;
    transition-delay: 0.3s;
    transition-duration: 500ms;
    position: relative;
    z-index: 999;
}

  .news {
    width: 85vw;
    height: 80vh;
    background-color: rgba(0, 0, 0, 0);
    position: absolute;
    top:calc(50vh - 40vh);
    right:calc(50vw - 42.5vw);
    z-index: 1;
  }

  .news p{
    font-family: mc-gamefont,serif;
    font-size: 40px;
    color: #c9ac67;
    margin-left: 5px;
  }



/*   导航栏   */

  .news .line {
    width: 100%;
    height: 2px;
    position: relative;
    background-color: #b5986a;
  }

  .news .line:nth-child(4){
    width: 80%;
  }

  .news .nav {
    width: 200px;
    height: 50px;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
  }

    .news .nav a {
      font-size: 15px;
      height: 10px;
      width: 50px;
      font-family: mc-gamefont, sans-serif;
      color: white;
      cursor: pointer;
    }

    .news .nav a:nth-child(1){
      margin-left: 20px;
    }

  .news .nav a:hover {
    color:  #c9ac67;
  }

    .news .nav a:hover div{
      width: 30px;
      height: 3px;
      background-color: #c9ac67;
      left:50px;
      transform: translateY(8px);
    }
  /*    背景    */

  .BG {
    background-image: url("@/assets/News/news-bg.jpg");
    width: 100%;
    height: 100%;
  }

  .footerBg {
    position: absolute;
    bottom: -2px;
    left: 0;
    z-index: 1;
    opacity: 0.5;
  }
  .footerBg video{
    width: 100%;
    height: 100%;
  }

  /*   新闻条目   */
.new  .newsContainer {
  width: 35%;
  height: 60%;
  position: absolute;
  top: 25%;
  left: 8%;
  z-index: 2;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.new .newsContainer .article {
  width: 100%;
  height: 16%;
  cursor: pointer;
}

.new .newsContainer .article:nth-child(1){
  height: 20%;
}

.new .newsContainer .article .lll{
  width: 100%;
  height: 1px;
  background-color: gray;
  position: relative;
  bottom: -45px;
  left: 0;
}

  .new .newsContainer .article .ll{
    width: 0;
    height: 5px;
    transition-delay: 500ms;
    transition: 1s;
    background-color: #c9ac67;
    position: relative;
    bottom: -45px;
    left: 0;
  }

  .new .newsContainer .article:hover .ll{
    width:100%;
  }

  .new .newsContainer .article p {
  border-radius: 50px;
  width: 50px;
  height: 25px;
  border:1px solid gray;
  position: relative;
  font-size: 15px;
  color: gray;
  display: inline-flex;
  justify-content: center;
  top: 40px;
}

  .new .newsContainer .article p:before{
    width: 5px;
    height: 5px;
    position: relative;
    content: ".";
    color: gray;
    font-size: 30px;
    top: -20px;
    left: -2px;
  }
  .new .newsContainer .article p:after{
    width: 5px;
    height: 5px;
    position: relative;
    content: ".";
    color: gray;
    font-size: 30px;
    top: -20px;
    right: 2px;
  }

  .new .newsContainer .article .message{
    width: 50%;
    height: 25%;
    position: relative;
    left: 20%;
    top: 5px;
    color: white;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
/*    轮播图    */
.new .router{
  position: absolute;
  top: 25%;
  left: 43%;
  z-index: 2;
  width: 50%;
  height: 60%;
}

.new .router img{
  width: 100%;
  height: 100%;
  padding: 2px;
  border: #c9ac67;
  border-radius: 0 25px 0 0;
}

.new .router img:nth-child(1){
  opacity: 1;
}
.new .router img:nth-child(2){
  opacity: 0;
}
</style>