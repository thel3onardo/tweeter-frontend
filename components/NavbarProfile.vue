<script setup lang="ts">
import { reactive } from 'vue'
import NavbarProfileMenu from './NavbarProfileMenu.vue';

defineProps<{
    profilePic: string
    username: string
}>();

const menu = reactive({ visible: false });

function openMenu() {
    menu.visible = !menu.visible;
}
</script>

<template>
  <div class="relative py-4">
      <div class="flex items-center">
        <div class="w-8 h-8 rounded overflow-hidden mr-2.5">
            <img :src="profilePic" class="object-cover h-full" v-once>
        </div>
        <h4 class="font-bold text-xs text-gray-800 font-noto-sans">{{ username }}</h4>
        <div class="material-icons text-xs ml-2 select-none cursor-pointer" @click="openMenu">arrow_drop_down</div>
        <NavbarProfileMenu v-if="menu.visible" />
    </div>
  </div>
</template>