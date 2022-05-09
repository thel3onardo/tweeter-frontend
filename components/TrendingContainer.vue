<template>
  <div class="w-80 px-5 bg-white flex flex-col rounded-xl">
      <span class="text-xs font-poppins font-semibold py-2 border-b border-gray-300">Trends for you</span>
      <TrendingItem v-for="item in trendingItems" :key="item.hashtag" :hashtag="item.hashtag" :interactions="item.interactions" />
  </div>
</template>

<script setup>
import { onMounted } from 'vue';

const trendingItems = ref();

onMounted(() => {
    trendingItems.value = [
        { hashtag: 'programming', interactions: 213 },
        { hashtag: 'devchallenges', interactions: 123 },
        { hashtag: 'frontend', interactions: 34 },
        { hashtag: 'helsinki', interactions: 11 },
        { hashtag: '100DaysOfCode', interactions: 5 },
        { hashtag: 'learntocode', interactions: 1 },
    ];
});

console.log(trendingItems.value)
</script>