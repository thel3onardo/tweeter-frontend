<script setup lang="ts">
import { reactive } from 'vue';

const profileOptions = reactive([
    { icon: 'account_circle', label: 'My profile' },
    { icon: 'group', label: 'Group chat' },
    { icon: 'settings', label: 'Settings' },
])
</script>

<template>
  <Transition name="menu-animation" appear>
        <div class="flex flex-col w-48 bg-white rounded-xl top-full right-0 absolute mt-1.5 py-4 px-3.5 shadow-lg">
            <div v-for="option in profileOptions" :key="option.label" class="flex items-center p-3 mb-3 hover:bg-gray-100 text-gray-700 rounded-xl cursor-pointer">
                <span class="material-icons mr-3">{{ option.icon }}</span>
                <span class="text-xs font-medium">{{ option.label }}</span>
            </div>
            <div class="h-px bg-gray-300"></div>
            <div class="flex items-center mt-4 p-3 rounded-xl text-red-500 hover:bg-red-100 cursor-pointer">
                <span class="material-icons mr-3">exit_to_app</span>
                <span class="text-xs font-medium">Logout</span>
            </div>
        </div>
    </Transition>
</template>

<style lang="scss" scoped>
.menu-animation-enter-active, .menu-animation-leave-active {
    transition: all .4s ease;
}

.menu-animation-enter-from, .menu-animation-leave-to {
    transform: translateY(15px);
    opacity: 0;
}
</style>