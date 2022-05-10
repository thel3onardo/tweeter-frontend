<template>
  <div class="w-full bg-white flex flex-col rounded-xl px-5 shadow">
      <h5 class="text-xs font-semibold font-poppins border-b border-gray-100 radius-xl py-2.5">Tweet something</h5>
      <div class="flex py-2">
          <div class="w-10 h-10 rounded-lg overflow-hidden">
              <img :src="props.profilePic" class="object-cover h-full">
          </div>
          <div class="flex flex-col justify-center items-center w-full">
              <form class="w-full" style="border: 1px solid red">
                  <textarea placeholder="What's happening?" style="border: 1px solid blue"></textarea>
              </form>
              <div class="w-full flex justify-between items-center">
                  <div class="flex text-blue-500">
                    <NewTweetReply />
                  </div>
                  <button class="text-white bg-blue-500 rounded px-7 py-1.5">Tweet</button>
              </div>
          </div>
      </div>
  </div>
</template>

<script setup>
const props = defineProps({
    profilePic: String,
})
</script>