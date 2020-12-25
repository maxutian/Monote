<template>
  <div class="flex border-b border-yellow-300 px-6 py-4 justify-between items-center cursor-pointer" :class="prefix">
    <p class=" text-gray-600 text-lg flex-1 hover:text-gray-900">{{article.title}}</p>
    <p class=" text-gray-400 text-sm">#{{article.index}}</p>
  </div>
</template>

<script lang="ts">
import { ref, PropType, defineComponent } from 'vue';

interface Article {
  id: string;
  title: string;
  index: number;
}

const ArticleBlock = defineComponent({
  props: {
    article: {
      type: Object as PropType<Article>,
      required: true,
    }
  },
  setup: () => {
    const prefix = ref<string>('article-block');

    return {
      prefix,
    }
  }
})

export default ArticleBlock;
</script>

<style lang="less">

</style>