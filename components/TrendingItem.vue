<script setup>
const props = defineProps({
    hashtag: {
        type: String,
        required: true,
    },
    interactions: {
        type: Number,
        required: true,
    }
})
</script>

<template>
    <div class="flex flex-col my-6 font-noto-sans">
        <h5 class="font-semibold">#{{props.hashtag}}</h5>
        <p class="font-medium text-gray-500">{{props.interactions}}k Tweets</p>
    </div>
</template>