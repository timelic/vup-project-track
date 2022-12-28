<script setup lang="ts">
import DotBg from "../assets/dot-bg.svg";
</script>

<template>
  <div class="winterstateful_dots" style="background-color: transparent">
    <img :src="DotBg" loading="lazy" alt="" />
  </div>
</template>

<style scoped>
.winterstateful_dots {
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  bottom: auto;
  z-index: -1;
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  overflow: hidden;
  width: 100%;
  height: 1780px;
  -webkit-box-pack: center;
  -webkit-justify-content: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-align: start;
  -webkit-align-items: flex-start;
  -ms-flex-align: start;
  align-items: flex-start;
  background-color: transparent;
  opacity: 1;
  -webkit-transition: opacity 0.8s;
  transition: opacity 0.8s;
  user-select: none;
  -webkit-user-drag: none;
}
</style>
