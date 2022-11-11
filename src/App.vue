<template>
  <child ref="childRef" />
</template>

<script lang="ts">
import { ref, onMounted } from "vue";
import child from "./components/child/index.vue";

export default {
  components: { child },
  setup() {
    let childRef = ref(null);
    onMounted(() => {
      console.log(child);
      console.log(child.value.name);
      console.log(child.value.age);
    });

    return { childRef };
  },
};
</script>

<style scoped>
</style>
