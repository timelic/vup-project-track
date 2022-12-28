<script lang="ts" setup>
import entryBg from "../assets/entry-bg.svg";
</script>

<template>
  <section>
    <h1>国内<span class="virtual">虚拟</span>社团现状追踪</h1>
    <div class="desc">
      一个专门收集整理国内虚拟社团的成员现状信息的网站。记录国内虚拟社团如虚研社、魂喵科技、战斗吧歌姬、星律动、雪风军团、哎咿多工作室、新科动漫、VirtuaReal等的成员情况。<br />所有信息均来源于B站公告或萌娘百科、论坛中的公开信息，不存在侵犯隐私的问题。
    </div>
    <img id="entry-bg" :src="entryBg" />
  </section>
</template>

<style lang="scss" scoped>
section {
  padding: 2rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  row-gap: 50px;
  padding-top: 200px;
  h1 {
    margin: 0;
    font-size: 54px;
    font-weight: bold;
    .virtual {
      background: linear-gradient(180deg, #1c99ff 0%, #0044ff 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
  }
  .desc {
    width: 740px;
    line-height: 40px;
    text-align: center;
  }
  #entry-bg {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1;
    opacity: 0.4;
    transform: translateY(-50px);
  }
}
</style>
