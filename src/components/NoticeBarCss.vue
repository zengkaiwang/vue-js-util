<template>
  <div class="wrap">
    <div class="cont">
      <p class="txt">1.文字如果超出了宽度自动向左滚动文字如果超出了宽度自动向左滚动。</p>
      <p class="txt">2.文字如果超出了宽度自动向左滚动文字如果超出了宽度自动向左滚动。</p>
    </div>
  </div>
</template>

<style lang="less" scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.wrap {
  position: relative;
  width: 40%;
  height: 40px;
  background: #ddd;
  overflow: hidden;
}
.wrap .cont {
  position: absolute;
  top: 0;
  left: 0;
  /* 宽度 大于容器的两倍即可 */
  width: 200%;
  -webkit-animation: 5s move infinite linear;
}
.wrap .txt {
  font-size: 18px;
  color: #fff;
  display: inline-block;
  /* 宽度 等于容器的宽度 */
  width: 50%;
  height: 30px;
  border-left: 1px solid #fff;
  line-height: 30px;
  text-align: center;
  margin-top: 5px;
  background: #000;
}
.wrap:hover .cont {
  -webkit-animation-play-state: paused;
}

@-webkit-keyframes move {
  /* 原理 left值的变化 移动一个容器的宽度 */
  0% {
    left: 0;
  }
  100% {
    left: -100%;
  }
}
</style>
