<template>
  <div class="flex justify-center pt-24 w-full h-screen" :class="prefix">
    <div class="w-3/12 mx-2 bg-white"></div>
    <div class="w-5/12 mx-2 bg-white"></div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup: () => {
    const prefix = ref('home');

    return {
      prefix
    }
  }
})
</script>

<style lang="less" scoped>
</style>