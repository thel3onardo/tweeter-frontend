<template>
  <div class="w-full bg-white flex flex-col rounded-xl px-5 shadow relative">
      <h5 class="text-xs font-semibold font-poppins border-b border-gray-100 radius-xl text-gray-700 py-2.5">Tweet something</h5>
      <div class="flex py-2">
          <div class="w-12 h-11 rounded-lg overflow-hidden mr-2">
              <img :src="props.profilePic" class="object-cover h-full">
          </div>
          <div class="flex flex-col justify-center items-center w-full">
              <form class="w-full mb-2">
                  <textarea placeholder="What's happening?" rows="2" class="h-full w-full py-2 outline-none"></textarea>
              </form>

              <div id="image-upload-preview" class="w-full"></div>

              <div class="w-full flex justify-between items-center">
                  <div class="flex items-center">
                      <NewTweetImageUpload />
                      <NewTweetConfig :current-config="tweetReplyConfig" />
                  </div>
                  <button class="text-white text-sm font-medium bg-blue-500 rounded px-7 py-1.5">Tweet</button>
              </div>
          </div>
      </div>
  </div>
</template>

<script setup>
const props = defineProps({
    profilePic: String,
})

const tweetReplyConfig = ref('everyone');
</script>