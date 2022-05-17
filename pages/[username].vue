<template>
  <div class="flex flex-col justify-center w-full">
    <div class="h-72 w-full bg-no-repeat bg-center bg-cover" :style="{'backgroundImage': `url('https://observatoriodoaudiovisual.com.br/wp-content/uploads/2020/08/32.jpg')`}"></div>
    <div class="flex justify-center" style="transform: translateY(-75px)">
      <div class="flex justify-between bg-white shadow px-6 pt-6 rounded-xl w-9/12">
        <div class="flex">
          <div class="h-40 w-40 border-4 border-white rounded-lg overflow-hidden mr-6" style="transform: translateY(-60px)">
            <img src="https://pbs.twimg.com/media/CslJ_1ZWgAEljbf.jpg" class="object-cover h-full" v-once>
          </div>
          <div class="flex flex-col">
            <div class="flex items-center font-poppins text-gray-800">
              <h1 class="text-2xl font-semibold mr-10">Daniel Jensen</h1>
              <p class="text-xs font-medium text-gray-500 mr-5">
                <span class="font-semibold text-gray-800">2,569</span>
                Following
              </p>
              <p class="text-xs font-medium text-gray-500 mr-5">
                <span class="font-semibold text-gray-800">10,8K</span>
                Followers
              </p>
            </div>
            <p class="text-lg my-8 text-gray-500 font-medium font-noto-sans">Teste meu deus cara nao aguento maisTeste meu deus cara nao aguento mais</p>
          </div>
        </div>
        <div>
          <button class="bg-blue-500 rounded text-white text-xs font-medium font-noto-sans px-6 py-2 flex items-center">
            <span class="material-icons text-lg mr-1">person_add</span>
            Follow
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>

</style>