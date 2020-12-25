<template>
  <div class="flex justify-center pt-24 w-full h-screen" :class="prefix">
    <div class="w-3/12 mx-2 pl-6 pr-16">
      <p class="text-right text-4xl">Monote</p>
      <p class="break-words text-right text-white my-7">Don't aim for success if you want it; just do what you love and believe in, and it will come naturally.</p>
      <ul class="text-right">
        <li class="nav-item">Home</li>
        <li class="nav-item">Tech</li>
        <li class="nav-item">Life</li>
        <li class="nav-item">Resume</li>
      </ul>
    </div>
    <div class="w-5/12 mx-2 bg-white shadow-lg rounded-t-md">
      <article-block v-for="article in articleList" :key="article.id" :article="article"></article-block>
    </div>
  </div>
</template>

<script lang="ts">
import { ref } from 'vue';
import ArticleBlock from '@/components/ArticleBlock.vue';

export default {
  setup: () => {
    const prefix = ref('home');
    const articleList = ref([{ id: 'fwegweg', title: 'My First Article', index: 1 }]);

    return {
      prefix,
      articleList,
    }
  },
  components: { "article-block": ArticleBlock }
}
</script>

<style lang="less">
  .nav-item {
    @apply my-2 text-yellow-400;
  }
</style>