<script setup>
import { Link } from '@inertiajs/vue3'

defineProps({
    image: String,
    title: String,
})
</script>

<template>
    <div class="mb-3 hover:bg-gray-100 cursor-pointer">
        <div class="flex items-start gap-2 py-2 px-2">
            <img :src="image" class="w-[32px] rounded-full">
            <div>
                <h3 class="font-black">{{ title }}</h3>
            </div>

        </div>
    </div>
</template>

<style scoped></style>
