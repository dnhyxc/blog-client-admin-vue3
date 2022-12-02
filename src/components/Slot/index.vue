<template>
  <div class="wrap">
    <div class="header">
      <slot name="header"></slot>
    </div>
    <div class="main">
      <div v-for="(item, index) in data">
        <slot :index="index" :data="item"></slot>
      </div>
    </div>
    <div class="footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";

type info = {
  auther: string;
  tag: string;
};

const data = reactive<info[]>([
  {
    auther: "dnhyxc",
    tag: "vue3",
  },
  {
    auther: "cxcx",
    tag: "react",
  },
  {
    auther: "wyhdxc",
    tag: "vite",
  },
]);
</script>

<style scoped lang="less">
.wrap {
  width: 100%;
  height: 100%;
  background-color: #fff;
  color: #333;

  .header {
    height: 200px;
    background-color: pink;
  }
  .main {
    height: 200px;
    background-color: greenyellow;
  }
  .footer {
    height: 200px;
    background-color: skyblue;
  }
}
</style>
