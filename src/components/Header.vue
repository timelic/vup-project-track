<script lang="ts" setup>
import Logo from "../assets/logo.svg";
</script>

<template>
  <header>
    <div class="left">
      <img :src="Logo" alt="logo" />
      <span>VupProjectTrack</span>
    </div>
    <div class="right">
      <span>引用</span>
      <span>开源</span>
      <span id="feedback-btn">信息反馈</span>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  position: fixed;
  z-index: 100;
  top: 0;
  left: 0;
  background: rgba(255, 255, 255, 0.4);
  backdrop-filter: blur(10px);
  width: 100vw;
  height: 72px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 14px;
  font-weight: 500;
  padding: 0 2rem;
  .left,
  .right {
    display: flex;
    align-items: center;
  }
  .left {
    column-gap: 1rem;
    cursor: pointer;
    // 后面会改一个字体
  }
  .right {
    column-gap: 1.5rem;
    span {
      cursor: pointer;
    }
  }
}
#feedback-btn {
  width: 84px;
  height: 36px;
  line-height: 36px;
  text-align: center;
  border-radius: 5px;
  background: linear-gradient(270deg, rgba(81, 103, 244, 1) 0%, #0084ff 100%);
  color: white;
  transition: 0.2s;
  &:hover {
    box-shadow: 0px 7px 10px -3px rgb(0 107 255 / 40%);
  }
}
</style>
