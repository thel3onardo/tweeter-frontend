<template>
  <div class="flex">
      <!-- <span class="material-icons">public</span> -->
      <div class="flex flex-col rounded-lg border borer-gray-300 px-3 shadow">
          <h5 class="text-xs text-gray-700 font-bold font-poppins mt-2 mb-1">Who can reply?</h5>
          <p class="text-xs font-noto-sans text-gray-500">Choose who can reply this Tweet.</p>
          <div class="flex flex-col my-3">
              <div v-for="option in configOptions" :key="option.label" class="flex items-center p-3 rounded-lg text-gray-700 hover:bg-gray-100 cursor-pointer">
                  <span class="material-icons mr-2">{{ option.icon }}</span>
                  <span class="text-xs font-medium font-noto-sans">{{ option.label }}</span>
              </div>
          </div>
      </div>
  </div>
</template>

<script setup>
defineProps({
    currentConfig: String
})

const configOptions = ref([
    { label: 'Everyone', icon: 'public' },
    { label: 'People you follow', icon: 'people' },
])
</script>