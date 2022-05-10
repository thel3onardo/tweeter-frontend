<template>
  <div class="flex items-center">
    <input type="file" accept="image/*" class="hidden" @change="handleFileInput" ref="fileInput">
    <button type="button" class="material-icons text-blue-500 cursor-pointer" @click="(e) => $refs['fileInput'].click()">image</button>
    <ClientOnly>
        <Teleport to="#image-upload-preview" v-if="imageFile">
            <div class="w-full h-96 my-5">
                <img :src="imagePreviewURL" class="object-cover w-full h-full rounded-xl">
            </div>
        </Teleport>
    </ClientOnly>
  </div>
</template>
<script setup>
const imageFile = ref(null);
const imagePreviewURL = ref(null);

function handleFileInput(e) {
    imageFile.value = e.target.files[0];
    imagePreviewURL.value = URL.createObjectURL(imageFile.value);
}
</script>