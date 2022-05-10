<template>
  <div class="w-full bg-white flex justify-between px-20">
      <div class="py-4">
          <img src="tweeter.svg" v-once>
      </div>
      <nav class="font-poppins">
          <ul class="flex h-full">
            <li v-for="item in navItems" :key="item.label" class="flex items-center mx-8 px-4 h-full font-medium text-sm text-gray-500 relative hover:text-blue-500 transition">
                <NuxtLink :to="item.href">{{ item.label }}</NuxtLink>
            </li>
        </ul>
      </nav>
      <div class="py-4">
          <NavbarProfile profile-pic="https://9tailedkitsune.com/wp-content/uploads/2021/04/zero-two_-cute.jpg" username="Leonardo" />
      </div>
  </div>
</template>

<script setup>
const navItems = ref([
    { label: 'Home', href: '/' },
    { label: 'Explore', href: '/explore' },
    { label: 'Bookmarks', href: '/bookmarks' }
]);
</script>

<style lang="scss" scoped>
    .router-link-exact-active {
        color: #2F80ED;
        font-weight: 600;

        &:before {
            content: "";
            width: 100%;
            height: 3px;
            background-color: #2F80ED;
            border-radius: 8px 8px 0px 0px;
            position: absolute;
            bottom: 0;
            left: 0;
        }
    }
</style>