<template>
  <div class="flex items-center">
      <div class="w-8 h-8 rounded overflow-hidden mr-2">
          <img :src="profilePic" class="object-cover h-full" v-once>
      </div>
      <h4 class="font-bold text-xs text-gray-800 font-noto-sans">{{ username }}</h4>
  </div>
</template>

<script setup lang="ts">
defineProps<{
    profilePic: string
    username: string
}>()
</script>