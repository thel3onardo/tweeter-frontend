<template>
  <div class="select-none">
    <div class="flex items-center justify-center text-blue-500 cursor-pointer" @click="openConfigMenu">
        <span class="material-icons h-5 w-5 mr-2">
            {{ currentConfig === 'everyone' ? 'public' : 'people'}}
        </span>
        <p class="text-xs mt-1">{{ currentConfig === 'everyone' ? 'Everyone can reply' : 'Only people you follow can reply'}}</p>
    </div>
    <div class="flex flex-col rounded-lg border border-gray-300 bg-white px-3 shadow absolute top-full" v-if="configMenuVisible">
        <h5 class="text-xs text-gray-700 font-bold font-poppins mt-2 mb-1">Who can reply?</h5>
        <p class="text-xs font-noto-sans text-gray-500">Choose who can reply this Tweet.</p>
        <div class="flex flex-col my-3">
            <div v-for="option in configOptions" :key="option.label" class="flex items-center p-3 rounded-lg text-gray-700 hover:bg-gray-100 cursor-pointer">
                <span class="material-icons mr-2">{{ option.icon }}</span>
                <p class="text-xs font-medium font-noto-sans">{{ option.label }}</p>
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
const configMenuVisible = ref(false);

const openConfigMenu = function() {
    console.log('a')
    configMenuVisible.value = !configMenuVisible.value;
}
</script>