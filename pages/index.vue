<template>
  <div class="h-screen flex justify-center my-6">
      <div class="flex">
        <div class="flex flex-col mr-6" style="width: 745px">
          <NewTweet profile-pic="https://9tailedkitsune.com/wp-content/uploads/2021/04/zero-two_-cute.jpg" />
        </div>
        <TrendingContainer />
      </div>
  </div>
</template>

<script setup>
  useHead({
    title: 'Tweeter - Home'
  });
</script>