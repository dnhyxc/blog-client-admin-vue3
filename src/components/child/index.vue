<template>
  <div>子组件</div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    let name = ref("dnhyxc");
    let age = ref(18);

    return { name, age };
  },
};
</script>