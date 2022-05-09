<template>
  <div class="w-full bg-white flex flex-col">
      <h5 class="text-xs font-semibold font-poppins border-b border-gray-100 radius-xl">Tweet something</h5>
      <div class="flex">
          <div>
              <img :src="props.profilePic">
          </div>
          <div class="flex flex-col">
              <form>
                  <textarea placeholder="What's happening?"></textarea>
              </form>
          </div>
      </div>
  </div>
</template>

<script setup>
const props = defineProps({
    profilePic: String,
})
</script>