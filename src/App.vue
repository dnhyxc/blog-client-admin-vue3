<template>
  <div class="app">
    <Home />
    <Slot>
      <template #header>
        <div>header</div>
      </template>
      <template #default="{ data, index }">
        <div>{{ data.auther }} -- {{ data.tag }} -- {{ index }}</div>
      </template>
      <template #footer>
        <div>footer</div>
      </template>
    </Slot>
  </div>
</template>

<script setup lang="ts">
import Slot from "./components/Slot/index.vue";
import Home from "./view/home/index.vue";
</script>

<style scoped lang="less">
.app {
  width: 100%;
  height: 100%;
  background-color: #fff;
  color: #333;
}
</style>
