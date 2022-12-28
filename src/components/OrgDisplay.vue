<script lang="ts" setup>
const info = {
  title: "A-SOUL",
  birthAndDeath: "2020年12月至今",
  desc: "A-SOUL是2020年11月23日公开的乐华娱乐旗下虚拟偶像团体，由字节跳动朝夕光年工作室负责技术支持和日常运营，主要于Bilibili和抖音上开展活动。",
  members: [
    {
      avator:
        "d399d6f5cf7943a996ae96999ba3e6ae2a2988de.jpg@240w_240h_1c_1s.webp",
      name: "嘉然",
    },
    {
      avator:
        "566078c52b408571d8ae5e3bcdf57b2283024c27.jpg@240w_240h_1c_1s.webp",
      name: "向晚",
    },
    {
      avator:
        "8895c87082beba1355ea4bc7f91f2786ef49e354.jpg@240w_240h_1c_1s.webp",
      name: "乃琳",
    },
    {
      avator: "668af440f8a8065743d3fa79cfa8f017905d0065.jpg",
      name: "贝拉",
    },
    {
      avator:
        "a7fea00016a8d3ffb015b6ed8647cc3ed89cbc63.jpg@240w_240h_1c_1s.webp",
      name: "珈乐",
      options: {
        quit: true,
      },
    },
  ],
};
</script>

<template>
  <div class="org-display">
    <div class="title">{{ info.title }}</div>
    <div class="birth-and-daeth">{{ info.birthAndDeath }}</div>
    <div class="desc">{{ info.desc }}</div>
    <div class="avator-group">
      <div class="avator-item" v-for="member in info.members">
        <img :src="`./avators/${member.avator}`" alt="" class="avator" />
        <img :src="`./avators/${member.avator}`" alt="" class="avator-shadow" />
        <div class="name">{{ member.name }}</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.org-display {
  margin: 200px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  row-gap: 20px;
  .title {
    font-size: 36px;
    font-weight: 700;
  }
  .birth-and-daeth {
    color: #999;
  }
  .desc {
    width: 680px;
    line-height: 2rem;
  }
  .avator-group {
    display: flex;
    column-gap: 1rem;
    .avator-item {
      position: relative;
      display: flex;
      flex-direction: column;
      row-gap: 1rem;
      .name {
        color: #333;
      }
      .avator {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background-color: #ccc;
        cursor: pointer;
        &:hover + .avator-shadow {
          opacity: 1;
        }
      }
      .avator-shadow {
        transition: 0.2s;
        width: 100px;
        height: 100px;
        border-radius: 50%;
        position: absolute;
        left: 0;
        top: 10px;
        z-index: -1;
        filter: blur(10px);
        opacity: 0;
      }
    }
  }
}
</style>
