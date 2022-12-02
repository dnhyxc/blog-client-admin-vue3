<!--
 * new page
 * @author: dnhyxc
 * @since: 2022-12-03
 * index.vue
-->
<template>
  <div class="container">
    <button @click="add">add+</button>
    <div class="content">{{ count }}</div>
    <button @click="subtract">subtract-</button>
  </div>
</template>

<script setup lang="ts">
import { ref, toRef, reactive } from "vue";

const count = ref(0);

const add = () => {
  count.value++;
};

const subtract = () => {
  count.value--;
};
</script>

<style scoped lang="less">
@import "./index.less";
</style>
